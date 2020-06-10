---
title: 'Operações e funções em p #'
description: Como definir e chamar operações e funções, bem como as especializações de operação controladas e adjacentes.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
ms.openlocfilehash: 6cfc1b14d86e86a1cbf0109d5e81dfe50c3a80bf
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630226"
---
# <a name="operations-and-functions-in-q"></a>Operações e funções em p #

## <a name="defining-new-operations"></a>Definindo novas operações

As operações são o núcleo de Q #.
Depois de declarados, eles podem ser chamados a partir de aplicativos .NET clássicos, por exemplo, usando um simulador ou por outras operações em Q #.
Cada operação definida em Q # pode então chamar qualquer número de outras operações, incluindo as operações intrínsecas internas definidas pelo idioma. A maneira específica em que essas operações intrínsecas são definidas depende da máquina de destino.
Quando compilada, cada operação é representada como um tipo de classe do .NET que pode ser fornecido para os computadores de destino.

Cada arquivo de origem Q # pode definir qualquer número de operações.
Os nomes de operação devem ser exclusivos em um namespace e podem não entrar em conflito com os nomes de tipo ou função.

Uma declaração de operação consiste na palavra-chave `operation` , seguida pelo símbolo que é o nome da operação, uma tupla de identificador tipada que define os argumentos para a operação, dois-pontos `:` , uma anotação de tipo que descreve o tipo de resultado da operação, opcionalmente uma anotação com as características da operação, uma chave `{` de abertura, o corpo da declaração da operação e uma chave de fechamento final `}` .

Cada operação usa uma entrada, produz uma saída e especifica a implementação para uma ou mais especializações de operação.
As especializações possíveis e como defini-las e chamá-las são detalhadas mais adiante.
Por enquanto, considere a seguinte operação, que define apenas uma especialização de corpo padrão e usa um único qubit como sua entrada e, em seguida, chama a <xref:microsoft.quantum.intrinsic.x> operação interna nessa entrada:

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

A palavra-chave `operation` começa a definição da operação e é seguida pelo nome; aqui, `BitFlip` .
Em seguida, o tipo da entrada é definido como `Qubit` , junto com um nome `target` para fazer referência à entrada dentro da nova operação.
Da mesma forma, o `Unit` define que a saída da operação está vazia.
Isso é usado da mesma forma `void` no C# e em outras linguagens imperativas e é equivalente a `unit` em F # e a outras linguagens funcionais.

As operações também podem retornar tipos mais interessantes do que `Unit` .
Por exemplo, a <xref:microsoft.quantum.intrinsic.m> operação retorna uma saída do tipo `Result` , representando tendo realizado uma medição. Podemos passar a saída de uma operação para outra operação ou pode usá-la com a `let` palavra-chave para definir uma nova variável.

Isso permite representar a computação clássica que interage com as operações Quantum em um nível baixo, como na [codificação superdensa](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):

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
> Cada operação em Q # usa exatamente uma entrada e retorna exatamente uma saída.
> Várias entradas e saídas são representadas usando *tuplas*, que coletam vários valores juntos em um único valor.
> Informalmente, dizemos que Q # é uma linguagem de "tupla na tupla".
> Após esse conceito, `()` deve ser lido como a tupla "vazia", que tem o tipo `Unit` .


## <a name="controlled-and-adjoint-operations"></a>Operações controladas e adjacentes

Se uma operação implementa uma transformação unitário, como é o caso de muitas operações em Q #, é possível definir como a operação age quando *adjointed* ou *controlada*. Uma especialização *adjacente* de uma operação especifica como o "inverso" da operação age, enquanto uma especialização *controlada* especifica como uma operação age quando seu aplicativo é condicionado no estado de um registro de Quantum específico.

Adjoints de operações Quantum são cruciais para muitos aspectos da computação Quantum. Além disso, na seção [conjugados](#conjugations) , você encontrará uma dessas situações discutida junto com uma técnica útil de programação de Q #.

A versão controlada de uma operação é uma nova operação que aplica efetivamente a operação base somente se todas as qubits de controle estiverem em um estado especificado.
Se o controle qubits estiver em superposição, a operação base será aplicada coerentemente à parte apropriada da superposição.
Portanto, as operações controladas geralmente são usadas para gerar Entanglement.

Naturalmente, uma especialização *adjacente controlada* poderia existir também, especificando o aplicativo controlado de um adjacente de uma operação.

> [!NOTE]
> Se $U $ for a transformação unitário implementada por uma operação `U` , `Adjoint U` o representará a transformação unitário $U ^ \dagger $, que é a transpoção conjugada complexa.
> Aplicar sucessivamente uma operação e, em seguida, seu adjacente a um estado deixa o estado inalterado, conforme ilustrado pelo fato de que $UU ^ \dagger = U ^ \dagger U = \id $, a matriz de identidade.
> A representação unitário de uma operação controlada é ligeiramente mais nuance, mas você pode encontrar mais detalhes em [conceitos de computação Quantum: vários qubits](xref:microsoft.quantum.concepts.multiple-qubits).

A seção a seguir descreve como chamar essas várias especializações no código Q #.
Abaixo, detalhamos como definir operações para dar suporte a eles.

### <a name="calling-operation-specializations"></a>Chamando especializações de operação

Um *functor* em Q # é um alocador que define uma nova operação de outra operação.
Os dois transmissão functors padrão em Q # são `Adjoint` e `Controlled` .

Transmissão functors têm acesso à implementação da operação base ao definir a implementação da nova operação.
Portanto, o transmissão functors pode executar funções mais complexas do que as funções tradicionais de nível superior. Transmissão functors não tem uma representação no sistema do tipo Q #. Portanto, no momento, não é possível associá-los a uma variável ou passá-los como argumentos. 

Um functor é usado aplicando-o a uma operação, retornando uma nova operação.
Por exemplo, a operação resultante da aplicação do `Adjoint` functor à `Y` operação é escrita como `Adjoint Y` .
A nova operação pode ser invocada como qualquer outra operação.
Para uma operação para dar suporte ao aplicativo do `Adjoint` e/ou `Controlled` transmissão functors, seu tipo de retorno precisa ser necessariamente `Unit` . 

#### <a name="adjoint-functor"></a>`Adjoint`functor

Assim, `Adjoint Y(q1)` o aplica o functor de modo adjacente à `Y` operação para gerar uma nova operação e aplica essa nova operação ao `q1` .
A nova operação tem a mesma assinatura e tipo que a operação base `Y` .
Em particular, a nova operação também permite e `Adjoint` permitirá `Controlled` se e somente se a operação base tivesse sido.
O functor de adjacente é seu próprio inverso; ou seja, `Adjoint Adjoint Op` é sempre o mesmo que `Op` .

#### <a name="controlled-functor"></a>`Controlled`functor

Da mesma forma, `Controlled X(controls, target)` o aplica o functor controlado à `X` operação para gerar uma nova operação e aplica essa nova operação ao `controls` e ao `target` .

> [!NOTE]
> Em Q #, as versões controladas sempre usam uma matriz de qubits de controle e o estado especificado é sempre para todos os qubits de controle que estão no estado computacional ( `PauliZ` ) `One` , $ \ket {1} $.
> O controle com base em outros Estados pode ser obtido aplicando a operação unitário apropriada ao qubits de controle antes da operação controlada e, em seguida, aplicando os inversos da operação unitário após a operação controlada.
> Por exemplo, aplicar uma `X` operação a um controle qubit antes e depois de uma operação controlada fará com que a operação controle o `Zero` estado ($ \ket {0} $) para esse qubit; aplicar uma `H` operação antes e depois controlará o `PauliX` `One` estado, que é-1 eigenvalue de Pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt {2} $ em vez do `PauliZ` `One` estado.

Dada uma expressão de operação, uma nova expressão de operação pode ser formada usando o `Controlled` functor.
A assinatura da nova operação é baseada na assinatura da operação original.
O tipo de resultado é o mesmo, mas o tipo de entrada é de duas tuplas com uma matriz qubit que mantém o controle qubit (s) como o primeiro elemento e os argumentos da operação original como o segundo elemento.
A nova operação dá suporte a `Controlled` e dará suporte a `Adjoint` If e somente se a operação original tiver feito isso.

Se a operação original levou apenas um único argumento, a equivalência de tupla singleton entrará em ação aqui.
Por exemplo, `Controlled X` é a versão controlada da `X` operação. 
`X`tem tipo `(Qubit => Unit is Adj + Ctl)` , portanto, `Controlled X` tem tipo `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` ; devido à equivalência de tupla singleton, isso é o mesmo que `((Qubit[], Qubit) => Unit is Adj + Ctl)` .

Se a operação base levou vários argumentos, lembre-se de colocar os argumentos correspondentes da versão controlada da operação entre parênteses para convertê-los em uma tupla.
Por exemplo, `Controlled Rz` é a versão controlada da `Rz` operação. 
`Rz`tem tipo `((Double, Qubit) => Unit is Adj + Ctl)` , portanto, `Controlled Rz` tem tipo `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .
Portanto, `Controlled Rz(controls, (0.1, target))` seria uma invocação válida de `Controlled Rz` (Observe os parênteses `0.1, target` ).

Como outro exemplo, `CNOT(control, target)` pode ser implementado como `Controlled X([control], target)` . Se um destino deve ser controlado por dois qubits de controle (CCNOT), podemos usar a `Controlled X([control1, control2], target)` instrução.

#### `Controlled Adjoint` 

O `Controlled` e o `Adjoint` transmissão functorsm o áudio, portanto, não há nenhuma diferença entre aplicar `Controlled Adjoint Op` ou `Adjoint Controlled Op` .


## <a name="defining-controlled-and-adjoint-implementations"></a>Definindo implementações controladas e adjacentes

Nos exemplos de declaração de primeira operação acima, as operações `BitFlip` e `DecodeSuperdense` foram definidas com assinaturas `(Qubit => Unit)` e `((Qubit, Qubit) => (Result, Result))` , respectivamente.
Como `DecodeSuperdense` inclui medições, ela não é uma operação unitário e, portanto, nenhuma especialização não adjacente pode existir (Lembre-se do requisito relacionado que tal operação retorna `Unit` ).
No entanto, como `BitFlip` simplesmente executa a <xref:microsoft.quantum.intrinsic.x> operação unitário, poderíamos defini-la com ambas as especializações.

Aqui, detalhamos como incluir a existência de especializações em suas declarações de operação de Q #, portanto, dando-lhes a capacidade de chamada em conjunto com o `Adjoint` and/or `Controlled` transmissão functors.
Além [disso,](#circumstances-for-validly-defining-specializations)descrevemos algumas das situações em que elas são válidas ou não válidas para declarar determinadas especializações.

As características da operação definem quais tipos de transmissão functors podem ser aplicados à operação declarada e qual efeito eles têm. A existência dessas especializações pode ser declarada como parte da assinatura da operação, especificamente por meio de uma anotação com as características da operação: `is Adj` `is Ctl` ou, ou `is Adj + Ctl` .
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
Portanto, podemos usar isso para escrever o `DecodeSuperdense` exemplo acima de forma mais compacta, usando o erro de `PrepareEntangledPair` para transformar o estado confusas de volta em um par unentangled de qubits:

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

No caso em que a implementação não pode ser gerada pelo compilador, ela pode ser especificada explicitamente. Essas declarações de especialização explícitas podem consistir em uma *diretiva de geração* adequada ou em uma implementação definida pelo usuário.
Aqui, fornecemos a gama completa de possibilidades, com exemplos a seguir.


#### <a name="explicit-specialization-declarations"></a>Declarações de especialização explícitas

As operações de Q # podem conter as seguintes declarações de especialização explícitas:

- A `body` especialização especifica a implementação da operação sem nenhum transmissão functors aplicado.
- A `adjoint` especialização especifica a implementação da operação com o `Adjoint` functor aplicado.
- A `controlled` especialização especifica a implementação da operação com o `Controlled` functor aplicado.
- A `controlled adjoint` especialização especifica a implementação da operação com o `Adjoint` e o `Controlled` transmissão functors aplicados.
  Essa especialização também pode ser nomeada `adjoint controlled` , já que as duas transmissão functorsm.


Uma especialização de operação consiste na marca de especialização (por exemplo `body` , ou `adjoint` , etc.) seguida de uma das:

- Uma declaração explícita, conforme descrito abaixo.
- Uma *diretiva* que informa ao compilador *como* gerar a especialização, uma das:
  - `intrinsic`, que indica que a especialização é fornecida pelo computador de destino.
  - `distribute`, que pode ser usado com as `controlled` `controlled adjoint` especializações e.
    Quando usado com `controlled` , ele indica que o compilador deve calcular a especialização aplicando-se `Controlled` a todas as operações no `body` .
    Quando usado com `controlled adjoint` , ele indica que o compilador deve calcular a especialização aplicando-se `Controlled` a todas as operações na `adjoint` especialização.
  - `invert`, que indica que o compilador deve calcular a `adjoint` especialização invertendo o `body` , ou seja, revertendo a ordem das operações e aplicando o adjacente a cada uma delas.
    Quando usado com `adjoint controlled` , isso indica que o compilador deve calcular a especialização invertendo a `controlled` especialização.
  - `self`, para indicar que a especialização de adjacente é a mesma que a `body` especialização.
    Isso é legal para as `adjoint` `adjoint controlled` especializações e.
    Para `adjoint controlled` , `self` implica que a `adjoint controlled` especialização é a mesma que a `controlled` especialização.
  - `auto`, para indicar que o compilador deve selecionar uma diretiva apropriada a ser aplicada.
    `auto`Não pode ser usado para a `body` especialização.

As diretivas e `auto` todas exigem um ponto-e-vírgula de fechamento `;` .
A `auto` diretiva será resolvida para a seguinte diretiva de geração se uma declaração explícita do `body` for fornecida:

- A `adjoint` especialização é gerada de acordo com a diretiva `invert` .
- A `controlled` especialização é gerada de acordo com a diretiva `distribute` .
- A `adjoint controlled` especialização será gerada de acordo com a diretiva `invert` se uma declaração explícita para `controlled` for fornecida, mas não uma para e `adjoint` , `distribute` caso contrário.

> [!TIP]   
> Se uma operação for autoadjacente, especifique explicitamente a prejunção ou a especialização de adjacente controlada por meio da diretiva de geração `self` para permitir que o compilador use essas informações para fins de otimização.

Uma declaração de especialização que contém uma implementação definida pelo usuário consiste em uma tupla de argumento seguida por um bloco de instrução com o código Q # que implementa a especialização.
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

O código `PrepareEntangledPair` acima, por exemplo, é equivalente ao código abaixo que contém declarações de especialização explícitas: 

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

Se o compilador não puder gerar a implementação para determinada especialização automaticamente ou se uma implementação mais eficiente puder ser fornecida, a implementação também poderá ser definida manualmente.

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
No exemplo acima, `adjoint invert;` indica que a especialização de adjacente deve ser gerada pela inversão da implementação do corpo e `controlled adjoint invert;` indica que a especialização adjacente controlada deve ser gerada por meio da inversão da implementação fornecida da especialização controlada.

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

É legal especificar uma operação sem nenhuma versão adjacente ou controlada. Por exemplo, as operações de medição não têm nenhum, porque elas não são invertível ou controláveis.

Uma operação dá suporte a `Adjoint` e/ou `Controlled` transmissão functors se sua declaração contiver uma declaração implícita ou explícita das respectivas especializações.

Uma especialização adjacente/controlada explícita implica a existência de uma especialização adjacente/controlada. 

Para uma operação cujo corpo contém loops repetir-até-êxito, instruções SET, medidas, instruções de retorno ou chamadas para outras operações que não dão suporte a `Adjoint` functor, a geração automática de uma especialização de adjacente após a `invert` `auto` diretiva ou não é possível.

Para uma operação cujo corpo contém chamadas para outras operações que não dão suporte ao `Controlled` functor, a geração automática de uma especialização controlada após a `distribute` `auto` diretiva ou não é possível.

#### <a name="controlled-adjoint"></a>Adjacente controlado

A versão adjacente controlada de uma operação especifica como uma versão controlada pelo Quantum do adjoin da operação é implementada.
É legal especificar uma operação sem nenhuma versão adjacente controlada; por exemplo, as operações de medição não têm nenhuma versão adjacente controlada porque não são controláveis nem invertível.

Uma especialização de adjacente controlada para uma operação precisa existir se e somente se houver uma especialização de somente um e um adjacente. Nesse caso, a existência da especialização adjacente controlada é inferida e uma especialização apropriada é gerada pelo compilador se nenhuma implementação tiver sido definida explicitamente. 

Para uma operação cujo corpo contém chamadas para outras operações que não têm uma versão adjacente controlada, a geração automática de uma especialização de adjacente após a `invert` `distribute` `auto` diretiva ou não é possível.


### <a name="type-compatibility"></a>Compatibilidade de tipo

Uma operação com suporte adicional a transmissão functors pode ser usada em qualquer lugar de uma operação com menos transmissão functors, mas a mesma assinatura é esperada.
Por exemplo, uma operação do tipo `(Qubit => Unit is Adj)` pode ser usada em qualquer lugar em que uma operação do tipo `(Qubit => Unit)` é esperada.

Q # é *covariant* com relação a tipos de retorno que podem ser chamados: um callable que retorna um tipo `'A` é compatível com um callable com o mesmo tipo de entrada e um tipo de resultado `'A` compatível com.

Q # é *contravariant* em relação aos tipos de entrada: um callable que usa um tipo `'A` como entrada é compatível com um callable com o mesmo tipo de resultado e um tipo de entrada compatível com `'A` .

Ou seja, dadas as seguintes definições:

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

o seguinte é verdadeiro:

- A função `ConjugateInvertWith` pode ser chamada com um `inner` argumento de `Invert` ou `ApplyUnitary` .
- A função `ConjugateUnitaryWith` pode ser chamada com um `inner` argumento de `ApplyUnitary` , mas não `Invert` .
- Um valor do tipo `(Qubit[] => Unit is Adj + Ctl)` pode ser retornado de `ConjugateInvertWith` .

> [!IMPORTANT]
> A p # 0,3 introduziu uma diferença significativa no comportamento de tipos definidos pelo usuário.

Os tipos definidos pelo usuário são tratados como uma versão encapsulada do tipo subjacente, em vez de como um subtipo.
Isso significa que um valor de um tipo definido pelo usuário não é utilizável, em que um valor do tipo subjacente é esperado.


### <a name="conjugations"></a>Conjugações

Em contraste com os bits clássicos, liberar memória Quantum é um pouco mais envolvida, uma vez que a redefinição oculta de qubits pode ter efeitos indesejados na computação restante se o qubits ainda for confusas. Isso pode ser evitado com o "desfazendo" adequadamente os cálculos executados antes de liberar a memória. Um padrão comum na computação Quantum é, portanto, o seguinte: 

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

A partir da nossa versão 0,9, damos suporte a uma instrução Conjugation que implementa a transformação acima. Usando essa instrução, a operação `ApplyWith` pode ser implementada da seguinte maneira:

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
Uma instrução de conjugação, obviamente, se torna muito mais útil se as transformações externa e interna não estão prontamente disponíveis como operações, mas são mais convenientes de descrever por um bloco que consiste em várias instruções. 

A transformação inversa para as instruções definidas no bloco Within é gerada automaticamente pelo compilador e executada após a conclusão do bloco de aplicação.
Como as variáveis mutáveis usadas como parte do bloco Within não podem ser reassociadas no bloco Apply, a transformação gerada é garantida como sendo a adjoin do cálculo no bloco Within. 


## <a name="defining-new-functions"></a>Definindo novas funções

As funções são puramente determinísticas, rotinas clássicas em Q #, que são diferentes das operações, pois elas não têm permissão para ter nenhum efeito além de calcular um valor de saída.
Em particular, as funções não podem chamar operações; agir sobre, alocar ou emprestar qubits; números aleatórios de exemplo; ou, de outra forma, dependem do estado após o valor de entrada para uma função.
Como consequência, as funções Q # são *puras*, pois elas sempre mapeiam os mesmos valores de entrada para os mesmos valores de saída.
Isso permite que o compilador Q # reordene com segurança como e quando as funções são chamadas ao gerar especializações de operação.

Cada arquivo de origem Q # pode definir qualquer número de funções.
Os nomes de função devem ser exclusivos em um namespace e podem não entrar em conflito com os nomes de operação ou tipo.

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

Sempre que for possível fazer isso, é útil escrever a lógica clássica em termos de funções em vez de operações, para que ela possa ser usada mais prontamente em operações.
Por exemplo, se tivéssemos escrito a `Square` declaração acima como uma *operação*, o compilador não teria conseguido garantir que chamá-la com a mesma entrada produziria consistentemente as mesmas saídas.

Para enfatizar a diferença entre funções e operações, considere o problema de amostragem clássica de um número aleatório de dentro de uma operação Q #:

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

Cada vez que `U` for chamado, ele terá uma ação diferente no `target` .
Em particular, o compilador não pode garantir que, se adicionamos uma `adjoint auto` declaração de especialização a `U` , `U(target); Adjoint U(target);` atua como identidade (ou seja, como não operacional).
Isso viola a definição do adjacente que vimos em [vetores e matrizes](xref:microsoft.quantum.concepts.vectors), de modo que permitir a geração automática de uma especialização adjacente em uma operação em que chamamos a operação <xref:microsoft.quantum.math.randomreal> interromperia as garantias fornecidas pelo compilador; <xref:microsoft.quantum.math.randomreal> é uma operação para a qual não existe nenhuma versão adjacente ou controlada.

Por outro lado, permitir chamadas de função como `Square` é seguro, pois o compilador pode ter certeza de que ele só precisa preservar a entrada para `Square` para manter sua saída estável.
Portanto, isolar o máximo de lógica clássica possível em funções facilita a reutilização dessa lógica em outras funções e operações semelhantes.


## <a name="generic-type-parameterized-callables"></a>Chamadores genéricos (com parâmetros de tipo)

Muitas funções e operações que desejamos definir não dependem muito dos tipos de suas entradas, mas, em vez disso, apenas usam implicitamente seus tipos por meio de alguma outra função ou operação.
Por exemplo, considere o conceito de *mapa* comum a muitas linguagens funcionais; dada uma função $f (x) $ e uma coleção de valores $ \{ x_1, x_2, \dots, x_n \} $, MAP retorna uma nova coleção $ \{ f (x_1), f (x_2), \dots, f (x_n) \} $.
Para implementar isso em Q #, podemos aproveitar essas funções como primeira classe.
Vamos escrever um exemplo rápido de `Map` , usando ★ como um espaço reservado enquanto configuramos quais tipos precisamos.

```qsharp
function Map(fn : (★ -> ★), values : ★[]) : ★[] {
    mutable mappedValues = new ★[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Observe que essa função parece muito boa, independentemente de quais tipos reais substituímos.
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

Em princípio, poderíamos escrever uma versão do `Map` para cada par de tipos que encontramos, mas isso apresenta uma série de dificuldades.
Por exemplo, se encontrarmos um bug no `Map` , devemos garantir que a correção seja aplicada uniformemente em todas as versões do `Map` .
Além disso, se construirmos uma nova tupla ou UDT, agora devemos também construir um novo `Map` para ir junto com o novo tipo.
Embora isso seja indevido a um pequeno número de funções desse tipo, à medida que coletamos cada vez mais funções da mesma forma que `Map` , o custo da introdução de novos tipos torna-se razoavelmente grande em ordem razoavelmente curta.

No entanto, grande parte dessa dificuldade resulta de que o compilador não deu as informações de que ele precisa para reconhecer como as diferentes versões do `Map` estão relacionadas.
Efetivamente, queremos que o compilador trate `Map` como um tipo de função matemática de *tipos* q # para funções q #.

Essa noção é formalizada permitindo que funções e operações tenham *parâmetros de tipo*, bem como seus parâmetros de tupla comuns.
Nos exemplos acima, desejamos considerar `Map` como tendo parâmetros de tipo `Int, Pauli` no primeiro caso e `Double, String` no segundo caso.
Na maior parte, esses parâmetros de tipo podem ser usados como se fossem tipos comuns: usamos valores de parâmetros de tipo para criar matrizes e tuplas, chamar funções e operações e atribuir a variáveis comuns ou mutáveis.

> [!NOTE]
> O caso mais extremo de dependência indireta é o de qubits, em que um programa Q # não pode depender diretamente da estrutura do `Qubit` tipo, mas **deve** passar esses tipos para outras operações e funções.

Retornando ao exemplo acima, podemos ver que precisamos `Map` ter parâmetros de tipo, um para representar a entrada para `fn` e um para representar a saída de `fn` .
Em Q #, isso é escrito pela adição de colchetes angulares (ou seja `<>` , não brakets $ \braket {} $!) após o nome de uma função ou operação em sua declaração e listando cada parâmetro de tipo.
O nome de cada parâmetro de tipo deve começar com um tique `'` , indicando que ele é um parâmetro de tipo e não um tipo comum (também conhecido como um tipo *concreto* ).
Por `Map` isso, escrevemos:

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Observe que a definição de `Map<'Input, 'Output>` parece extremamente semelhante às versões que escrevemos antes.
A única diferença é que nós informamos explicitamente o compilador que `Map` não depende diretamente do `'Input` que e `'Output` são, mas funciona para dois tipos usando-os indiretamente por meio de `fn` .
Depois de definirmos `Map<'Input, 'Output>` dessa forma, podemos chamá-lo como se fosse uma função comum:

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> Escrever funções e operações genéricas é um lugar em que "tupla-in-out" é uma maneira muito útil de pensar em funções e operações do Q #.
> Como cada função usa exatamente uma entrada e retorna exatamente uma saída, uma entrada do tipo `'T -> 'U` corresponde a *qualquer* função Q # qualquer.
> Da mesma forma, qualquer operação pode ser passada para uma entrada do tipo `'T => 'U` .

Como um segundo exemplo, considere o desafio de escrever uma função que retorne a composição de duas outras funções:

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Aqui, devemos especificar exatamente o que `A` , `B` e `C` estão, limitando seriamente o utilitário de nossa nova `Compose` função.
Afinal, `Compose` só depende de `A` , `B` e `C` *através* `innerFn` de e `outerFn` .
Como alternativa, podemos adicionar parâmetros de tipo ao `Compose` que indiquem que ele funciona para *qualquer* `A` , `B` e `C` , desde que esses parâmetros correspondam aos esperados por `innerFn` e `outerFn` :

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

As bibliotecas padrão de Q # fornecem uma variedade de operações e funções parametrizadas por tipo para facilitar o expressar o fluxo de controle de ordem mais alta.
Eles são abordados mais detalhadamente no [Guia de biblioteca padrão do Q #](xref:microsoft.quantum.libraries.standard.intro).


## <a name="callables-as-first-class-values"></a>É chamado como valores de primeira classe

Uma técnica crítica para o raciocínio sobre o fluxo de controle e a lógica clássica usando funções em vez de operações é utilizar essas operações e funções em Q # são de *primeira classe*.
Ou seja, eles são cada um dos valores no idioma que estão no seu próprio direito.
Por exemplo, este é um código Q # perfeitamente válido, se um pouco indireto:

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

O valor da variável `ourH` no trecho acima é, então, a operação <xref:microsoft.quantum.intrinsic.h> , de modo que podemos chamar esse valor como qualquer outra operação.
Isso nos permite escrever operações que usam operações como parte de sua entrada, formando conceitos de fluxo de controle de ordem mais alta.
Por exemplo, podemos imaginar que queira "quadrado" uma operação aplicando-a duas vezes ao mesmo qubit de destino.

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a>Retornando operações de uma função

Enfatizamos que também podemos retornar operações como parte das saídas, de modo que possamos isolar alguns tipos de lógica condicional clássica como uma função clássica que retorna uma descrição de um programa Quantum na forma de uma operação.
Como exemplo simples, considere o exemplo de teleportação, no qual a parte que recebe uma mensagem clássica de dois bits precisa usar a mensagem para decodificar seu qubit no estado de Teleporta adequado.
Poderíamos escrever isso em termos de uma função que pega esses dois bits clássicos e retorna a operação de decodificação adequada.

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

Essa nova função é realmente uma função, já que, se o chamarmos com os mesmos valores de `hereBit` e `thereBit` , sempre retornaremos a mesma operação.
Assim, o decodificador pode ser executado com segurança dentro de operações sem ter que ter por motivo de como a lógica de decodificação interage com as definições das diferentes especializações de operação.
Ou seja, isolamos a lógica clássica dentro de uma função, garantindo ao compilador que a chamada de função pode ser reordenada com impunity, desde que a entrada seja preservada.


## <a name="partial-application"></a>Aplicativo parcial

Podemos fazer significativamente mais com funções que retornam operações usando o *aplicativo parcial*, no qual podemos fornecer uma ou mais partes da entrada a uma função ou operação sem realmente chamá-la. Por exemplo, rechamar o `ApplyTwice` exemplo acima, podemos indicar que não queremos especificar, imediatamente, a qual qubit a operação de entrada deve ser aplicada:

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

Nesse caso, a variável local `twiceOp` mantém a operação parcialmente aplicada `ApplyTwice(op, _)` , em que partes da entrada que ainda não foram especificadas são indicadas por `_` .
Quando realmente chamamos `twiceOp` na próxima linha, passamos como entrada para a operação parcialmente aplicada todas as partes restantes da entrada para a operação original.
Portanto, o trecho acima é efetivamente idêntico a ter chamado `ApplyTwice(op, target)` diretamente, salvar para que tenhamos introduzido uma nova variável local que nos permite atrasar a chamada enquanto fornece algumas partes da entrada.

Como uma operação que foi parcialmente aplicada não é realmente chamada até que toda a sua entrada tenha sido fornecida, podemos aplicar operações parcialmente de forma segura, mesmo a partir de funções.

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

Em princípio, a lógica clássica dentro `SquareOperation` poderia ter sido muito mais envolvida, mas ainda é isolada do restante de uma operação pelas garantias que o compilador pode oferecer sobre as funções.
Essa abordagem será usada em toda a biblioteca padrão de Q # para expressar o fluxo de controle clássico de forma que possa ser prontamente usada em programas Quantum.


## <a name="recursion"></a>Recursão

Os chamadores do Q # podem ser recursivos direta ou indiretamente.
Ou seja, uma operação ou função pode chamar a si mesma ou chamar outro callable que chama direta ou indiretamente a operação que pode ser chamada.

No entanto, há dois comentários importantes sobre o uso da recursão:

- O uso da recursão nas operações provavelmente interfere em determinadas otimizações.
  Isso pode ter um impacto significativo no tempo de execução do algoritmo.
- Ao executar em um dispositivo Quantum real, o espaço de pilha pode ser limitado e, portanto, a recursão profunda pode levar a um erro de tempo de execução.
  Em particular, o compilador e o tempo de execução do Q # não identificam e otimizam a recursão da cauda.

## <a name="next-steps"></a>Próximas etapas

Saiba mais sobre [variáveis](xref:microsoft.quantum.guide.variables) em Q #.