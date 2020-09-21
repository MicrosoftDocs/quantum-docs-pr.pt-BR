---
title: Operações e funções no Q#
description: Como definir e chamar operações e funções, bem como as especializações de operação controladas e adjacentes.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
no-loc:
- Q#
- $$v
ms.openlocfilehash: c2ce999ea2a0fe7204f402fedb4cd3a3c15bd44b
ms.sourcegitcommit: 8256ff463eb9319f1933820a36c0838cf1e024e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/17/2020
ms.locfileid: "90759417"
---
# <a name="operations-and-functions-in-no-locq"></a>Operações e funções no Q#

## <a name="defining-new-operations"></a>Definindo novas operações

As operações são o núcleo de Q# .
Depois de declarados, eles podem ser chamados de aplicativos .NET clássicos, por exemplo, usando um simulador ou outras operações no Q# .
Cada operação definida no Q# pode chamar qualquer número de outras operações, incluindo as operações intrínsecas internas definidas pelo idioma. A maneira específica de Q# definir essas operações intrínsecas depende da máquina de destino.
Quando compilada, cada operação é representada como um tipo de classe do .NET que pode ser fornecido para os computadores de destino.

Cada Q# arquivo de origem pode definir qualquer número de operações.
Os nomes de operação devem ser exclusivos em um namespace e não podem entrar em conflito com nomes de tipo ou função.

Uma declaração de operação consiste na palavra-chave `operation` , seguida pelo símbolo que é o nome da operação, uma tupla de identificador tipada que define os argumentos para a operação, dois-pontos `:` , uma anotação de tipo que descreve o tipo de resultado da operação, opcionalmente uma anotação com as características da operação, uma chave de abertura e o corpo da declaração da operação, entre chaves `{ }` .

Cada operação usa uma entrada, produz uma saída e especifica a implementação para uma ou mais especializações de operação.
As especializações possíveis e como defini-las e chamá-las são detalhadas nas diferentes seções deste artigo.
Por enquanto, considere a seguinte operação, que define apenas uma especialização de corpo padrão e usa um único qubit como sua entrada e, em seguida, chama a <xref:microsoft.quantum.intrinsic.x> operação interna nessa entrada:

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

A palavra-chave `operation` começa a definição da operação, seguida pelo nome; aqui, `BitFlip` .
Em seguida, o tipo de entrada é definido ( `Qubit` ), junto com um nome, `target` , para se referir à entrada dentro da nova operação.
Por fim, `Unit` define que a saída da operação está vazia.
`Unit` é usado da mesma forma `void` no C# e em outras linguagens imperativas e é equivalente a `unit` em F # e a outras linguagens funcionais.

As operações também podem retornar tipos mais interessantes do que `Unit` .
Por exemplo, a <xref:microsoft.quantum.intrinsic.m> operação retorna uma saída do tipo `Result` , representando tendo realizado uma medição.  Você pode passá-lo de uma operação para outra operação ou usá-lo com a `let` palavra-chave para definir uma nova variável.

Essa abordagem permite representar a computação clássica que interage com as operações Quantum em um nível baixo, como na [codificação superdensa](https://github.com/microsoft/QuantumKatas/tree/main/SuperdenseCoding):

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

> [!NOTE]
> Cada operação no Q# usa exatamente uma entrada e retorna exatamente uma saída.
> Várias entradas e saídas são representadas usando *tuplas*, que coletam vários valores juntos em um único valor.
> Nesse sentido, Q# é uma linguagem de "tupla na tupla".
> Após esse conceito, um conjunto de parênteses vazios, `()` , deve ser lido como a tupla "vazia", que tem o tipo `Unit` .

## <a name="controlled-and-adjoint-operations"></a>Operações controladas e adjacentes

Se uma operação implementa uma transformação unitário, como é o caso de muitas operações no Q# , é possível definir como a operação age quando *adjointed* ou *controlada*. Uma especialização *adjacente* de uma operação especifica como o "inverso" da operação age, enquanto uma especialização *controlada* especifica como uma operação age quando seu aplicativo é condicionado no estado de um registro de Quantum específico.

Adjoints de operações Quantum são cruciais para muitos aspectos da computação Quantum. Para obter um exemplo de uma dessas situações discutida junto com uma Q# técnica de programação útil, consulte [conjugados](#conjugations) neste artigo. 

A versão controlada de uma operação é uma nova operação que aplica efetivamente a operação base somente se todas as qubits de controle estiverem em um estado especificado.
Se o controle qubits estiver em superposição, a operação base será aplicada coerentemente à parte apropriada da superposição.
Portanto, as operações controladas geralmente são usadas para gerar Entanglement.

Naturalmente, uma especialização *adjacente controlada* poderia existir também, especificando o aplicativo controlado de um adjacente de uma operação.

> [!NOTE]
> Se $U $ for a transformação unitário implementada por uma operação `U` , `Adjoint U` o representará a transformação unitário $U ^ \dagger $, que é a transpoção conjugada complexa.
> Aplicar sucessivamente uma operação e, em seguida, seu adjacente a um estado deixa o estado inalterado, conforme ilustrado pelo fato de que $UU ^ \dagger = U ^ \dagger U = \id $, a matriz de identidade.
> A representação unitário de uma operação controlada é ligeiramente mais nuance, mas você pode encontrar mais detalhes em [conceitos de computação Quantum: vários qubits](xref:microsoft.quantum.concepts.multiple-qubits).

A seção a seguir descreve como chamar essas várias especializações em seu Q# código e como definir operações para dar suporte a elas.

### <a name="calling-operation-specializations"></a>Chamando especializações de operação

Um *functor* no Q# é uma fábrica que define uma nova operação de outra operação.
Os dois transmissão functors padrão no Q# são `Adjoint` e `Controlled` .

Transmissão functors têm acesso à implementação da operação base ao definir a implementação da nova operação.
Portanto, o transmissão functors pode executar funções mais complexas do que as funções tradicionais de nível superior. Transmissão functors não tem uma representação no sistema de Q# tipos. Portanto, no momento, não é possível associá-los a uma variável ou passá-los como argumentos. 

Use um functor aplicando-o a uma operação, que retorna uma nova operação.
Por exemplo, aplicar o `Adjoint` functor à `Y` operação retorna a nova operação `Adjoint Y` . Você pode invocar a nova operação como qualquer outra operação.
Para uma operação para dar suporte ao aplicativo do `Adjoint` ou `Controlled` transmissão functors, seu tipo de retorno precisa ser necessariamente `Unit` . 

#### <a name="adjoint-functor"></a>`Adjoint` functor

Assim, `Adjoint Y(q1)` o aplica o `Adjoint` functor à `Y` operação para gerar uma nova operação e aplica essa nova operação ao `q1` .
A nova operação tem a mesma assinatura e tipo que a operação base `Y` .
Em particular, a nova operação também dá suporte a e `Adjoint` dá suporte a `Controlled` If e somente se a operação base tiver feito.
O `Adjoint` functor é seu próprio inverso; ou seja, `Adjoint Adjoint Op` é sempre o mesmo que `Op` .

#### <a name="controlled-functor"></a>`Controlled` functor

Da mesma forma, `Controlled X(controls, target)` o aplica o `Controlled` functor à `X` operação para gerar uma nova operação e aplica essa nova operação ao `controls` e ao `target` .

> [!NOTE]
> No Q# , as versões controladas sempre assumem uma matriz de qubits de controle e o controle é sempre baseado em todos os qubits de controle que estão no `PauliZ` estado computacional () `One` , $ \ket {1} $.
> O controle com base em outros Estados é obtido aplicando a operação unitário apropriada ao qubits de controle antes da operação controlada e, em seguida, aplicando as inversas da operação unitário após a operação controlada.
> Por exemplo, a aplicação de uma `X` operação a um qubit de controle antes e depois de uma operação controlada faz com que a operação controle o `Zero` estado ($ \ket {0} $) para esse qubit; a aplicação de uma `H` operação antes e depois dos controles no `PauliX` `One` estado, que é-1 eigenvalue de Pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt {2} $ em vez do `PauliZ` `One` estado.

Dada uma expressão de operação, você pode formar uma nova expressão de operação usando o `Controlled` functor.
A assinatura da nova operação é baseada na assinatura da operação original.
O tipo de resultado é o mesmo, mas o tipo de entrada é de duas tuplas com uma matriz qubit que mantém o controle qubit (s) como o primeiro elemento e os argumentos da operação original como o segundo elemento.
A nova operação dá suporte a `Controlled` e dará suporte a `Adjoint` If e somente se a operação original tiver feito isso.

Se a operação original levou apenas um único argumento, a [equivalência de tupla singleton](xref:microsoft.quantum.guide.types) entra em cena aqui.
Por exemplo, `Controlled X` é a versão controlada da `X` operação. 
`X` tem tipo `(Qubit => Unit is Adj + Ctl)` , portanto, `Controlled X` tem tipo `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` ; devido à equivalência de tupla singleton, isso é o mesmo que `((Qubit[], Qubit) => Unit is Adj + Ctl)` .

Se a operação base levou vários argumentos, lembre-se de colocar os argumentos correspondentes da versão controlada da operação entre parênteses para convertê-los em uma tupla.
Por exemplo, `Controlled Rz` é a versão controlada da `Rz` operação. 
`Rz` tem tipo `((Double, Qubit) => Unit is Adj + Ctl)` , portanto, `Controlled Rz` tem tipo `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .
Portanto, `Controlled Rz(controls, (0.1, target))` seria uma invocação válida de `Controlled Rz` (Observe os parênteses `0.1, target` ).

Como outro exemplo, `CNOT(control, target)` pode ser implementado como `Controlled X([control], target)` . Se um destino deve ser controlado por dois qubits de controle (CCNOT), use uma `Controlled X([control1, control2], target)` instrução.

#### `Controlled Adjoint` 

O `Controlled` e o `Adjoint` transmissão functorsm o áudio, portanto, não há nenhuma diferença entre aplicar `Controlled Adjoint Op` ou `Adjoint Controlled Op` .


## <a name="defining-controlled-and-adjoint-implementations"></a>Definindo implementações controladas e adjacentes

Na primeira declaração de operação nos exemplos anteriores, as operações `BitFlip` e `DecodeSuperdense` foram definidas com assinaturas `(Qubit => Unit)` e `((Qubit, Qubit) => (Result, Result))` , respectivamente.
Como `DecodeSuperdense` inclui medições, ela não é uma operação unitário e, portanto, nenhuma especialização não adjacente pode existir (Lembre-se do requisito relacionado que tal operação retorna `Unit` ).
No entanto, como `BitFlip` simplesmente executa a <xref:microsoft.quantum.intrinsic.x> operação unitário, você poderia defini-la com ambas as especializações.

Esta seção fornece detalhes sobre como incluir a existência de especializações em suas Q# declarações de operação, portanto, dando-lhes a capacidade de chamada em conjunto com o `Adjoint` ou `Controlled` transmissão functors.
Para obter mais informações sobre algumas das situações em que elas são válidas ou não válidas para declarar determinadas especializações, consulte [circunstâncias de definição válida de especializações](#circumstances-for-validly-defining-specializations) neste artigo.

As características da operação definem quais tipos de transmissão functors você pode aplicar à operação declarada e qual efeito eles têm. A existência dessas especializações pode ser declarada como parte da assinatura da operação, especificamente por meio de uma anotação com as características da operação: `is Adj` `is Ctl` ou, ou `is Adj + Ctl` .
A implementação real de cada especialização pode ser definida *implicitamente* ou *explicitamente* .

### <a name="implicitly-specifying-implementations"></a>Especificando implicitamente implementações

Nesse caso, o corpo da declaração da operação consiste exclusivamente na implementação padrão. Por exemplo:

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
Aqui, a implementação correspondente para cada uma dessas especializações declaradas implicitamente é gerada automaticamente pelo compilador, a ser executada se o `Adjoint` ou `Controlled` transmissão functors forem usados.

Portanto, uma chamada de `Adjoint PrepareEntangledPair` resultaria no compilador que implementasse o adpositivo de `CNOT` e, em seguida, o adjacente de `H` .
Essas operações individuais são autoadjacentes, portanto, a operação resultante `Adjoint PrepareEntangledPair` simplesmente consistiria em aplicar `CNOT(here, there)` e depois `H(here)` .
Portanto, você pode usar isso para escrever o `DecodeSuperdense` no exemplo anterior mais compactamente, usando o adjoin de `PrepareEntangledPair` para transformar o estado confusas de volta em um par unentangled de qubits:

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

A anotação com as características da operação na declaração é útil para garantir que o compilador gere automaticamente outras especializações com base na implementação padrão. 

Há várias limitações importantes a serem consideradas ao criar operações para uso com o transmissão functors.
O mais importante é que as especializações para uma operação que usa o valor de saída de qualquer outra operação *não podem* ser geradas automaticamente pelo compilador, pois é ambígua como reordenar as instruções nessa operação para obter o mesmo efeito.

Portanto, geralmente é útil especificar explicitamente as várias implementações.

### <a name="explicitly-specifying-implementations"></a>Especificando explicitamente implementações

No caso em que o compilador não pode gerar a implementação, você pode especificá-lo explicitamente. Essas declarações de especialização explícitas podem consistir em uma *diretiva de geração* adequada ou em uma implementação definida pelo usuário.
A seguir, há uma gama completa de possibilidades, com alguns exemplos de especialização explícita. 


#### <a name="explicit-specialization-declarations"></a>Declarações de especialização explícitas

Q# as operações podem conter as seguintes declarações de especialização explícitas:

- A `body` especialização especifica a implementação da operação sem nenhum transmissão functors aplicado.
- A `adjoint` especialização especifica a implementação da operação com o `Adjoint` functor aplicado.
- A `controlled` especialização especifica a implementação da operação com o `Controlled` functor aplicado.
- A `controlled adjoint` especialização especifica a implementação da operação com o `Adjoint` e o `Controlled` transmissão functors aplicados.
  Essa especialização também pode ser nomeada `adjoint controlled` , já que as duas transmissão functorsm.


Uma especialização de operação consiste na marca de especialização (por exemplo, `body` ou `adjoint` ) seguida de uma das:

- Uma declaração explícita, conforme descrito a seguir.
- Uma *diretiva* que informa ao compilador *como* gerar a especialização, uma das:
  - `intrinsic`, que indica que o computador de destino fornece a especialização.
  - `distribute`, usado com as `controlled` `controlled adjoint` especializações e.
    Quando usado com `controlled` , ele indica que o compilador deve calcular a especialização aplicando-se `Controlled` a todas as operações no `body` .
    Quando usado com `controlled adjoint` , ele indica que o compilador deve calcular a especialização aplicando-se `Controlled` a todas as operações na `adjoint` especialização.
  - `invert`, que indica que o compilador deve calcular a `adjoint` especialização invertendo o `body` , por exemplo, revertendo a ordem das operações e aplicando o adjacente a cada uma delas.
    Quando usado com `adjoint controlled` , isso indica que o compilador deve calcular a especialização invertendo a `controlled` especialização.
  - `self`, para indicar que a especialização de adjacente é igual à `body` especialização.
    Usar `self` o é legal para `adjoint` as `adjoint controlled` especializações e.
    Para `adjoint controlled` , `self` implica que a `adjoint controlled` especialização é a mesma que a `controlled` especialização.
  - `auto`, para indicar que o compilador deve selecionar uma diretiva apropriada a ser aplicada.
    Você não pode usar `auto` para a `body` especialização.

As diretivas e `auto` todas exigem um ponto-e-vírgula de fechamento `;` .
A `auto` diretiva será resolvida para a seguinte diretiva gerada se uma declaração explícita do `body` for fornecida:

- A `adjoint` especialização gera de acordo com a diretiva `invert` .
- A `controlled` especialização gera de acordo com a diretiva `distribute` .
- A `adjoint controlled` especialização gera de acordo com a diretiva `invert` se uma declaração explícita para `controlled` é fornecida, mas não uma para `adjoint` , e de `distribute` outra forma.

> [!TIP]   
> Se uma operação for autoadjacente, especifique explicitamente a prejunção ou a especialização de adjacente controlada por meio da diretiva de geração `self` para permitir que o compilador use essas informações para fins de otimização.

Uma declaração de especialização que contém uma implementação definida pelo usuário consiste em uma tupla de argumento seguida por um bloco de instrução com o Q# código que implementa a especialização.
Na lista de argumentos, `...` é usado para representar os argumentos declarados para a operação como um todo.
Para `body` e `adjoint` , a lista de argumentos deve ser sempre `(...)` ; para `controlled` e `adjoint controlled` , a lista de argumentos deve ser um símbolo que representa a matriz de controle qubits, seguida por `...` , entre parênteses; por exemplo, `(controls,...)` .

### <a name="examples"></a>Exemplos

Uma declaração de operação pode ser tão simples quanto a seguinte, que define a operação primitiva de Pauli X:

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
Observe que o adjoin da operação Pauli X é definido com a diretiva `self` porque, por definição, `X` é seu próprio inverso.

No exemplo anterior `PrepareEntangledPair` , o código é equivalente ao seguinte código que contém declarações de especialização explícitas: 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
A palavra-chave `auto` indica que o compilador deve determinar como gerar a implementação de especialização.

#### <a name="user-defined-specialization-implementation"></a>Implementação de especialização definida pelo usuário

Se o compilador não puder gerar a implementação para determinada especialização automaticamente ou se uma implementação mais eficiente puder ser fornecida, você poderá definir manualmente a implementação.

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user-defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
No exemplo anterior, `adjoint invert;` indica que a especialização de adjacente deve ser gerada pela inversão da implementação do corpo e `controlled adjoint invert;` indica que a especialização adjacente controlada deve ser gerada pela inversão da implementação fornecida da especialização controlada.

Se uma ou mais especializações além do corpo padrão precisarem ser declaradas explicitamente, a implementação do corpo padrão precisará ser encapsulada em uma declaração de especialização adequada também:

```qsharp
operation CountOnes(qubits: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (qubit in qubits) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="circumstances-for-validly-defining-specializations"></a>Circunstâncias de definição válida de especializações

#### <a name="operation-declarations-with-adjointcontrolled"></a>Declarações de operação com adjoind/controlled

É legal especificar uma operação sem nenhuma versão adjacente ou controlada. Por exemplo, as operações de medição não têm porque elas não são invertível ou controláveis.

Uma operação dá suporte a `Adjoint` e `Controlled` transmissão functors se sua declaração contiver uma declaração implícita ou explícita das respectivas especializações.

Uma especialização adjacente/controlada explícita implica a existência de uma especialização adjacente/controlada. 

Para uma operação cujo corpo contém loops repetir-até-êxito, instruções SET, medidas, instruções de retorno ou chamadas para outras operações que não dão suporte a `Adjoint` functor, a geração automática de uma especialização de adjacente após a `invert` `auto` diretiva ou não é possível.

Para uma operação cujo corpo contém chamadas para outras operações que não dão suporte ao `Controlled` functor, a geração automática de uma especialização controlada após a `distribute` `auto` diretiva ou não é possível.

#### <a name="controlled-adjoint"></a>Adjacente controlado

A versão adjacente controlada de uma operação especifica como implementar uma versão controlada pelo Quantum do adjoin da operação.
É legal especificar uma operação sem nenhuma versão adjacente controlada; por exemplo, as operações de medição não têm nenhuma versão adjacente controlada porque não são controláveis nem invertível.

Uma especialização de adjacente controlada para uma operação precisa existir se e somente se houver uma especialização de somente um e um adjacente. Nesse caso, a existência da especialização adjacente controlada é inferida. Se nenhuma implementação for definida explicitamente, a compilação gerará uma especialização apropriada.

Para uma operação cujo corpo contém chamadas para outras operações que não têm uma versão adjacente controlada, a geração automática de uma especialização de adjacente após a `invert` `distribute` diretiva, ou `auto` não é possível.


### <a name="type-compatibility"></a>Compatibilidade de tipo

Use uma operação com transmissão functors adicionais com suporte em qualquer lugar em que você use uma operação com menos transmissão functors, mas a mesma assinatura. Por exemplo, use uma operação do tipo `(Qubit => Unit is Adj)` em qualquer lugar em que você use uma operação do tipo `(Qubit => Unit)` .

Q# é *Covariance* com relação a tipos de retorno que podem ser chamados: um callable que retorna um tipo `'A` é compatível com um callable com o mesmo tipo de entrada e um tipo de resultado compatível com `'A` .

Q# é *contravariant* em relação aos tipos de entrada: um callable que usa um tipo `'A` como entrada é compatível com um callable com o mesmo tipo de resultado e um tipo de entrada compatível com `'A` .

Ou seja, dadas as definições a seguir,

```qsharp
operation Invert(qubits : Qubit[]) : Unit 
is Adj {...} 

operation ApplyUnitary(qubits : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertWith(
    inner : (Qubit[] => Unit is Adj),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith(
    inner : (Qubit[] => Unit is Adj + Ctl),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

É possível

- Invoque a função `ConjugateInvertWith` com um `inner` argumento de `Invert` ou `ApplyUnitary` .
- Invocar a função `ConjugateUnitaryWith` com um `inner` argumento de `ApplyUnitary` , mas não `Invert` .
- Retornar um valor do tipo `(Qubit[] => Unit is Adj + Ctl)` de `ConjugateInvertWith` .

> [!IMPORTANT]
> Q# 0,3 introduziu uma diferença significativa no comportamento de tipos definidos pelo usuário.

Os tipos definidos pelo usuário são tratados como uma versão encapsulada do tipo subjacente, em vez de como um subtipo.
Isso significa que um valor de um tipo definido pelo usuário não é utilizável em que você espera que um valor do tipo subjacente seja.


### <a name="conjugations"></a>Conjugações

Em contraste com os bits clássicos, liberar memória Quantum é um pouco mais envolvida, uma vez que a redefinição oculta de qubits pode ter efeitos indesejados na computação restante se o qubits ainda for confusas. Esses efeitos podem ser evitados de forma adequada "desfazer" as computações realizadas antes de liberar a memória. Um padrão comum na computação Quantum é, portanto, o seguinte: 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

A partir da nossa versão 0,9, Q# o dá suporte a uma instrução de conjugação que implementa a transformação anterior. Usando essa instrução, a operação `ApplyWith` pode ser implementada da seguinte maneira:

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
Essa instrução de conjugação se torna muito mais útil se as transformações externas e internas não estão prontamente disponíveis como operações, mas são mais convenientes de descrever por um bloco consistindo em várias instruções. 

A transformação inversa para as instruções definidas no bloco Within é gerada automaticamente pelo compilador e executada após a conclusão do bloco de aplicação.
Como as variáveis mutáveis usadas como parte do bloco Within não podem ser reassociadas no bloco Apply, a transformação gerada é garantida como sendo a adjoin do cálculo no bloco Within. 


## <a name="defining-new-functions"></a>Definindo novas funções

As funções são puramente determinísticas, rotinas clássicas no Q# , que são diferentes das operações, pois elas não têm permissão para ter nenhum efeito além de calcular um valor de saída.
Em particular, as funções não podem chamar operações; agir sobre, alocar ou emprestar qubits; números aleatórios de exemplo; ou, de outra forma, dependem do estado após o valor de entrada para uma função.
Como consequência, as Q# funções são *puras*, pois elas sempre mapeiam os mesmos valores de entrada para os mesmos valores de saída.
Esse comportamento permite que o Q# compilador reordene com segurança como e quando chamar funções ao gerar especializações de operação.

Cada Q# arquivo de origem pode definir qualquer número de funções.
Os nomes de função devem ser exclusivos em um namespace e não podem entrar em conflito com os nomes de operação ou tipo.

A definição de uma função funciona de forma semelhante à definição de uma operação, exceto que nenhuma especialização adjacente ou controlada pode ser definida para uma função.
Por exemplo:

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

ou 

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```

### <a name="classical-logic-in-functions--good"></a>Lógica clássica em funções = = bom

Sempre que for possível fazer isso, é útil escrever a lógica clássica em termos de funções em vez de operações para que as operações possam usá-las mais prontamente. Por exemplo, se você tivesse escrito a `Square` declaração anterior como uma *operação*, o compilador não teria conseguido garantir que chamá-la com a mesma entrada produzirá consistentemente as mesmas saídas.

Para enfatizar a diferença entre funções e operações, considere o problema de amostragem clássica de um número aleatório de dentro de uma Q# operação:

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

Cada vez que `U` é chamado, ele tem uma ação diferente em `target` .
Em particular, o compilador não pode garantir que, se você adicionar uma `adjoint auto` declaração de especialização a `U` , `U(target); Adjoint U(target);` atue como identidade (ou seja, como não operacional).
Isso viola a definição do adjoin definido em [vetores e matrizes](xref:microsoft.quantum.concepts.vectors), de modo que permitir que o compilador gere automaticamente uma especialização adjacente em uma operação na qual você chama a operação <xref:microsoft.quantum.math.randomreal> interromperia as garantias fornecidas pelo compilador; <xref:microsoft.quantum.math.randomreal> é uma operação para a qual não existe nenhuma versão adjacente ou controlada.

Por outro lado, permitir que chamadas de função, como `Square` é seguro, e garante ao compilador que ele só precisa preservar a entrada para `Square` manter sua saída estável.
Portanto, isolar o máximo de lógica clássica possível em funções facilita a reutilização dessa lógica em outras funções e operações semelhantes.


## <a name="generic-type-parameterized-callables"></a>Chamadores genéricos (com parâmetros de tipo)

Muitas funções e operações que você talvez queira definir não dependem muito dos tipos de suas entradas, mas, em vez disso, apenas usam implicitamente seus tipos por meio de alguma outra função ou operação.
Por exemplo, considere o conceito de *mapa* comum a muitas linguagens funcionais; dada uma função $f (x) $ e uma coleção de valores $ \{ x_1, x_2, \dots, x_n \} $, MAP retorna uma nova coleção $ \{ f (x_1), f (x_2), \dots, f (x_n) \} $.
Para implementar isso no Q# , aproveite o fato de que as funções são a primeira classe.
Aqui está um exemplo rápido de `Map` , usando `T` como um espaço reservado enquanto você descobrir quais tipos são necessários.

```qsharp
function Map(fn : (T -> T), values : T[]) : T[] {
    mutable mappedValues = new T[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Observe que essa função parece muito semelhante, independentemente de quais tipos reais você substitui.
Um mapa de inteiros para Paulis, por exemplo, parece muito o mesmo que um mapa de números de ponto flutuante para cadeias de caracteres:

```qsharp
function MapIntsToPaulis(fn : (Int -> Pauli), values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : (Double -> String), values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Em princípio, você poderia escrever uma versão do `Map` para cada par de tipos que encontrar, mas isso apresenta várias dificuldades.
Por exemplo, se você encontrar um bug no `Map` , deverá garantir que a correção seja aplicada uniformemente em todas as versões do `Map` .
Além disso, se você construir uma nova tupla ou UDT, agora você também deve construir um novo `Map` para ir junto com o novo tipo.
Embora isso seja indesejado para um pequeno número dessas funções, à medida que você coleta cada vez mais funções da mesma forma que `Map` , o custo da introdução de novos tipos torna-se razoavelmente grande em ordem razoavelmente curta.

No entanto, grande parte dessa dificuldade resulta do fato de que você não deu ao compilador as informações de que ele precisa para reconhecer como as diferentes versões do `Map` estão relacionadas.
Efetivamente, você deseja que o compilador trate `Map` como algum tipo de função matemática de Q# *tipos* para Q# funções.

Q# formalizes essa noção permitindo que funções e operações tenham *parâmetros de tipo*, bem como seus parâmetros de tupla comuns.
Nos exemplos anteriores, você deseja considerar `Map` como tendo parâmetros de tipo `Int, Pauli` no primeiro caso e `Double, String` no segundo caso.
Para a maior parte, use esses parâmetros de tipo como se fossem tipos comuns. Use valores de parâmetros de tipo para criar matrizes e tuplas, chamar funções e operações e atribuir a variáveis comuns ou mutáveis.

> [!NOTE]
> O caso mais extremo de dependência indireta é o de qubits, em que um Q# programa não pode depender diretamente da estrutura do `Qubit` tipo, mas **deve** passar esses tipos para outras operações e funções.

Retornando ao exemplo anterior, você vê que `Map` precisa ter parâmetros de tipo, um para representar a entrada para `fn` e um para representar a saída de `fn` .
No Q# , isso é escrito pela adição de colchetes angulares (isto é `<>` , não brakets $ \braket {} $!) após o nome de uma função ou operação em sua declaração e listando cada parâmetro de tipo.
O nome de cada parâmetro de tipo deve começar com um tique `'` , indicando que ele é um parâmetro de tipo e não um tipo comum (também conhecido como um tipo *concreto* ).
Portanto, `Map` , é escrito:

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Observe que a definição de `Map<'Input, 'Output>` parece extremamente semelhante às versões do previoius.
A única diferença é que você informou explicitamente o compilador que `Map` não depende diretamente do que `'Input` e `'Output` são, mas funciona para dois tipos usando-os indiretamente por meio de `fn` .
Depois de definido `Map<'Input, 'Output>` dessa forma, você pode chamá-lo como se fosse uma função comum:

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> Escrever funções e operações genéricas é um lugar em que "tupla-in-out" é uma maneira muito útil de pensar em Q# funções e operações.
> Como cada função usa exatamente uma entrada e retorna exatamente uma saída, uma entrada do tipo `'T -> 'U` corresponde a *qualquer* Q# função.
> Da mesma forma, você pode passar qualquer operação para uma entrada do tipo `'T => 'U` .

Como um segundo exemplo, considere o desafio de escrever uma função que retorne a composição de duas outras funções:

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Aqui, você deve especificar exatamente o que `A` , `B` e `C` estão, limitando seriamente o utilitário de nossa nova `Compose` função.
Afinal, `Compose` só depende de `A` , `B` e `C` *através* `innerFn` de e `outerFn` .
Como alternativa, você pode adicionar parâmetros de tipo ao `Compose` que indicam que ele funciona para *qualquer* `A` , `B` e `C` , desde que esses parâmetros correspondam aos esperados por `innerFn` e `outerFn` :

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

As Q# bibliotecas padrão fornecem uma variedade de operações e funções parametrizadas por tipo para facilitar o expressar o fluxo de controle de ordem mais alta.
Eles são discutidos mais detalhadamente no [ Q# guia da biblioteca padrão](xref:microsoft.quantum.libraries.standard.intro).


## <a name="callables-as-first-class-values"></a>É chamado como valores de primeira classe

Uma técnica crítica para o raciocínio sobre o fluxo de controle e a lógica clássica usando funções em vez de operações é utilizar essas operações e funções no Q# são de *primeira classe*.
Ou seja, eles são cada um dos valores no idioma que estão no seu próprio direito.
Por exemplo, o código a seguir é perfeitamente válido Q# , se for um pouco indireto:

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

O valor da variável `ourH` no trecho anterior é, então, a operação <xref:microsoft.quantum.intrinsic.h> , de modo que você pode chamar esse valor como qualquer outra operação.
Com essa capacidade, você pode gravar operações que usam operações como parte de sua entrada, formando conceitos de fluxo de controle de ordem superior.
Por exemplo, você pode imaginar que queira "quadrado" uma operação aplicando-a duas vezes ao mesmo qubit de destino.

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a>Retornando operações de uma função

É importante enfatizar que você também pode retornar operações como parte das saídas, de modo que você pode isolar alguns tipos de lógica condicional clássica como uma função clássica, que retorna uma descrição de um programa Quantum na forma de uma operação.
Como exemplo simples, considere o exemplo de teleportação, no qual a parte que recebe uma mensagem clássica de dois bits precisa usar a mensagem para decodificar seu qubit no estado de Teleporta adequado.
Você poderia escrever isso em termos de uma função que usa esses dois bits clássicos e retorna a operação de decodificação apropriada.

```qsharp
function TeleporationDecoderForMessage(hereBit : Result, thereBit : Result)
: (Qubit => Unit is Adj + Ctl) {

    if (hereBit == Zero && thereBit == Zero) {
        return I;
    } elif (hereBit == One && thereBit == Zero) {
        return X;
    } elif (hereBit == Zero && thereBit == One) {
        return Z;
    } else {
        return Y;
    }
}
```

Essa nova função é realmente uma função, se você chamá-la com os mesmos valores de `hereBit` e `thereBit` , sempre obterá a mesma operação.
Assim, o decodificador pode ser executado com segurança dentro de operações sem ter que ter em razão de como a lógica de decodificação interage com as definições das diferentes especializações de operação.
Ou seja, a lógica clássica dentro de uma função é isolada, garantindo ao compilador que a chamada de função pode ser reordenada com impunity, desde que a entrada seja preservada.


## <a name="partial-application"></a>Aplicativo parcial

Você pode fazer significativamente mais com funções que retornam operações usando o *aplicativo parcial*, no qual você fornece uma ou mais partes da entrada para uma função ou operação sem realmente chamá-la. No exemplo anterior `ApplyTwice` , você pode indicar que não deseja especificar, imediatamente, a qual qubit a operação de entrada deve ser aplicada:

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

Nesse caso, a variável local `twiceOp` contém a operação parcialmente aplicada `ApplyTwice(op, _)` , em que `_` indica partes da entrada que ainda não foram especificadas.
Quando você chama `twiceOp` na próxima linha, passa como entrada para a operação parcialmente aplicada todas as partes restantes da entrada para a operação original.
Assim, o trecho anterior é efetivamente idêntico a ter chamado `ApplyTwice(op, target)` diretamente, salvar para que você tenha introduzido uma nova variável local para que possa atrasar a chamada enquanto fornece algumas partes da entrada.

Como uma operação que foi parcialmente aplicada não é realmente chamada até que toda a sua entrada tenha sido fornecida, você pode aplicar operações parcialmente de forma segura, mesmo a partir de funções.

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

Em princípio, a lógica clássica dentro `SquareOperation` poderia ter sido muito mais envolvida, mas ainda é isolada do restante de uma operação pelas garantias que o compilador pode oferecer sobre as funções. A Q# biblioteca padrão usa essa abordagem para expressar o fluxo de controle clássico de forma que os programas Quantum possam ser usados prontamente.


## <a name="recursion"></a>Recursão

Q# os chamadores podem ser recursivos direta ou indiretamente.
Ou seja, uma operação ou função pode chamar a si mesma ou chamar outro callable que chama direta ou indiretamente a operação que pode ser chamada.

No entanto, há dois comentários importantes sobre o uso da recursão:

- O uso da recursão nas operações provavelmente interfere em determinadas otimizações.
  Essa interferência pode ter um impacto significativo no tempo de execução do algoritmo.
- Durante a execução em um dispositivo Quantum real, o espaço de pilha pode ser limitado e, portanto, a recursão profunda pode levar a um erro de tempo de execução.
  Em particular, o Q# compilador e o tempo de execução não identificam e otimizam a recursão de cauda.

## <a name="next-steps"></a>Próximas etapas

Saiba mais sobre [variáveis](xref:microsoft.quantum.guide.variables) no Q# .