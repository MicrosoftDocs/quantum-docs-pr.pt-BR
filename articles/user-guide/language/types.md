---
title: 'Tipos em p #'
description: 'Saiba mais sobre os diferentes tipos usados na linguagem de programação Q #.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
ms.openlocfilehash: 58370193bd62e306197a9e07c28f8611f043e55c
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431131"
---
# <a name="types-in-q"></a>Tipos em p #

Esta página cria o modelo de tipo Q # e descreve a sintaxe para especificar e trabalhar com tipos.
A próxima página, [digite expressões](xref:microsoft.quantum.guide.expressions), detalha como criar e operar em expressões desses tipos.

Observe que Q # é uma linguagem *fortemente tipada* , de modo que o uso cuidadoso desses tipos pode ajudar o compilador a fornecer fortes garantias sobre programas do Q # no momento da compilação.
Para fornecer as garantias mais fortes possíveis, as conversões entre os tipos em Q # devem ser explícitas usando chamadas para funções que expressam essa conversão. Uma variedade dessas funções é fornecida como parte do <xref:microsoft.quantum.convert> namespace.
Os upcasts para tipos compatíveis, por outro lado, acontecem implicitamente. 

O Q # fornece os dois tipos primitivos, que podem ser usados diretamente e várias maneiras de produzir novos tipos de outros tipos.
Descrevemos cada um no restante desta seção.

## <a name="primitive-types"></a>Tipos primitivos

A linguagem Q # fornece vários *tipos primitivos*, dos quais outros tipos podem ser construídos:

- O `Int` tipo representa um número inteiro com sinal de 64 bits, por exemplo: `2` , `107` , `-5` .
- O `BigInt` tipo representa um inteiro assinado de tamanho arbitrário, por exemplo,, `2L` `107L` `-5L` .
   Esse tipo é baseado no .NET<xref:System.Numerics.BigInteger>
   Escreva.
- O `Double` tipo representa um número de ponto flutuante de precisão dupla, por exemplo: `0.0` , `-1.3` , `4e-7` .
- O `Bool` tipo representa um valor booliano que pode ser `true` ou `false` .
- O `Range` tipo representa uma sequência de inteiros, denotada por `start..step..stop` , em que indica que a etapa é opções. 
   Que `start .. stop` corresponde a `start..1..stop` e, por exemplo, `1..2..7` representa a sequência $ \{ 1, 3, 5, 7 \} $.
- O `String` tipo é uma sequência de caracteres Unicode que é opaca para o usuário depois de criado.
  Esse tipo é usado para relatar mensagens a um host clássico no caso de um erro ou evento de diagnóstico.
- O `Unit` tipo é o tipo que permite apenas um valor `()` . 
  Esse tipo é usado para indicar que a função ou operação Q # não retorna nenhuma informação. 
- O `Qubit` tipo representa um bit quântico ou qubit.
   `Qubit`os s são opacos para o usuário; a única operação possível com eles, além de passá-los para outra operação, é testar a identidade (igualdade).
   Por fim, as ações em `Qubit` s são implementadas chamando instruções intrínsecas em um processador Quantum (ou em uma simulação delas).
- O `Pauli` tipo representa um dos quatro operadores de Pauli de qubit único.
   Esse tipo é usado para indicar a operação base para rotações e para especificar o observável que está sendo medido.
   Este é um tipo enumerado que tem quatro valores possíveis: `PauliI` , `PauliX` , `PauliY` e `PauliZ` , que são constantes do tipo `Pauli` .
- O `Result` tipo representa o resultado de uma medida.
   Este é um tipo enumerado com dois valores possíveis: `One` e `Zero` , que são constantes do tipo `Result` .
   `Zero`indica que a eigenvalue + 1 foi medida; `One`indica o-1 eigenvalue.

As constantes,,,,,, `true` `false` `PauliI` `PauliX` `PauliY` `PauliZ` `One` e `Zero` são todos os símbolos reservados em Q #.

## <a name="array-types"></a>Tipos de matriz

Dado qualquer tipo válido de Q # `'T` , há um tipo que representa uma matriz de valores do tipo `'T` .
Esse tipo de matriz é representado como `'T[]` ; por exemplo, `Qubit[]` ou `Int[][]` .
Por exemplo, uma coleção de inteiros é denotada `Int[]` , enquanto uma matriz de matrizes de `(Bool, Pauli)` valores é denotada `(Bool, Pauli)[][]` .

No segundo exemplo, observe que isso representa uma matriz potencialmente irregular de matrizes e não uma matriz bidimensional retangular.
O Q # não fornece suporte para matrizes multidimensionais retangulares.

Um valor de matriz pode ser escrito em código-fonte Q # usando colchetes em volta dos elementos de uma matriz, como em `[PauliI, PauliX, PauliY, PauliZ]` .
O tipo de um literal de matriz é determinado pelo tipo base comum de todos os itens na matriz. 

> [!WARNING]
> Os elementos de uma matriz não podem ser alterados após a criação da matriz.
> As [instruções UPDATE-and-REASSIGN](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) e/ou as [expressões Copy-and-Update](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) podem ser usadas para construir uma matriz modificada.

Como alternativa, uma matriz pode ser criada com base em seu tamanho usando a `new` palavra-chave:

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

Em ambos os casos, após a construção de uma matriz, a função principal `Length` pode ser usada para obter o número de elementos como um `Int` .
As matrizes podem ser subscritos usando colchetes, com subscritos que têm tipo `Int` ou tipo `Range` , para obter elementos únicos ou novas matrizes que contenham um subconjunto dos elementos de uma matriz.
Os subscritos das matrizes são baseados em zero:

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a>Tipos de tupla

Dado zero ou mais tipos diferentes `T0` , `T1` ,..., `Tn` , podemos indicar um novo *tipo de tupla* como `(T0, T1, ..., Tn)` .
Os tipos usados para construir um novo tipo de tupla podem ser tuplas, como em `(Int, (Qubit, Qubit))` .
No entanto, esse aninhamento é sempre finito, pois os tipos de tupla não podem, sob nenhuma circunstância, conter.

Os valores do novo tipo de tupla são tuplas formadas por sequências de valores de cada tipo na tupla.
Por exemplo, `(3, false)` é uma tupla cujo tipo é o tipo de tupla `(Int, Bool)` .
É possível criar matrizes de tuplas, tuplas de matrizes, tuplas de subtuplas, etc.

A partir de Q # 0,3, `Unit` é o nome do *tipo* da tupla vazia; `()` é usado para o *valor*de tupla vazio.

As instâncias de tupla são imutáveis.
O Q # não fornece um mecanismo para alterar o conteúdo de uma tupla depois de criada.

As tuplas são um conceito poderoso usado em toda a p # para coletar valores juntos em um único valor, facilitando sua passagem.
Em particular, usando a notação de tupla, podemos expressar que cada operação e que pode ser chamado leva exatamente uma entrada e retorna exatamente uma saída.

### <a name="singleton-tuple-equivalence"></a>Equivalência de tupla singleton

É possível criar uma tupla singleton (elemento único), como `('T1)` `(5)` ou `([1,2,3])` .
No entanto, Q # trata uma tupla singleton como totalmente equivalente a um valor do tipo incluído.
Ou seja, não há nenhuma diferença entre `5` e `(5)` , ou entre `5` e `(((5)))` , ou entre `(5, (6))` e `(5, 6)` .
Ele é tão válido para gravar `(5)+3` como gravar `5+3` e as duas expressões serão avaliadas como `8` .

Essa equivalência aplica-se a todas as finalidades, incluindo atribuições e expressões.
Dada qualquer expressão, a mesma expressão entre parênteses é uma expressão do mesmo tipo.
Por exemplo, `(7)` é uma `Int` expressão, `([1,2,3])` é uma expressão do tipo matriz de `Int` s e `((1,2))` é uma expressão com tipo `(Int, Int)` .

Em particular, isso significa que uma operação ou função cuja tupla de entrada ou tipo de tupla de saída tem um campo pode ser considerada como um único argumento ou retornando um único valor.

Nós nos referimos a essa propriedade como _equivalência de tupla singleton_.


## <a name="user-defined-types"></a>Tipos definidos pelo usuário

Uma declaração de tipo definida pelo usuário consiste na palavra-chave `newtype` , seguida pelo nome do tipo definido pelo usuário, uma `=` especificação de tipo válida e um ponto-e-vírgula de terminação.

Por exemplo:

```qsharp
newtype PairOfInts = (Int, Int);
```

Cada arquivo de origem Q # pode declarar qualquer número de tipos definidos pelo usuário.
Os nomes de tipo devem ser exclusivos em um namespace e podem não entrar em conflito com os nomes de operação e de função.

Os tipos definidos pelo usuário são distintos mesmo se os tipos base forem idênticos.
Em particular, não há conversão automática entre valores de dois tipos definidos pelo usuário, mesmo que os tipos subjacentes sejam idênticos.

### <a name="named-vs-anonymous-items"></a>Itens nomeados vs. anônimos

Um arquivo Q # pode definir um novo tipo nomeado contendo um único valor de qualquer tipo legal.
Para qualquer tipo de tupla `T` , podemos declarar um novo tipo definido pelo usuário que seja um subtipo de `T` com a `newtype` instrução.
No @"microsoft.quantum.math" namespace, por exemplo, números complexos são definidos como um tipo definido pelo usuário:

```qsharp
newtype Complex = (Double, Double);
```
Essa instrução cria um novo tipo com dois itens anônimos do tipo `Double` .   

Além de itens anônimos, os tipos definidos pelo usuário também dão suporte a *itens nomeados* a partir do Q # versão 0,7 ou superior. Por exemplo, poderíamos ter nomeado o to Items `Re` para o Double representando a parte real de um número complexo e `Im` para a parte imaginária: 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Nomear um item em um tipo definido pelo usuário não significa que todos os itens precisam ser nomeados-qualquer combinação de itens nomeados e sem nome é suportada. Além disso, os itens internos também podem ser nomeados.
O tipo `Nested` conforme definido abaixo, por exemplo, tem um tipo subjacente `(Double, (Int, String))` , do qual apenas o item do tipo `Int` é nomeado e todos os outros itens são anônimos. 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

Os itens nomeados têm a vantagem de que eles podem ser acessados diretamente por meio do *operador de acesso* `::` . 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

Além de fornecer aliases curtos para tipos de tupla potencialmente complicadas, uma vantagem significativa de definir esses tipos é que eles podem documentar a intenção de um valor específico.
Retornando ao exemplo de `Complex` , um também poderia ter definido as coordenadas polares 2D como um tipo definido pelo usuário:

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

Embora ambos `Complex` `Polar` tenham um tipo subjacente `(Double, Double)` , os dois tipos são totalmente incompatíveis em Q #, minimizando o risco de chamar acidentalmente uma função matemática complexa com coordenadas polares e vice-versa.
Dessa forma, os tipos definidos pelo usuário têm uma função semelhante à de registros em F #, por exemplo. 


#### <a name="access-anonymous-items-with-the-unwrap-operator"></a>Acessar itens anônimos com o operador de desencapsulamento

Para acessar itens anônimos por outro lado, o valor encapsulado primeiro precisa ser extraído usando o operador de sufixo `!` .
O operador "Unwrap", `!` , permite extrair o valor contido em um tipo definido pelo usuário.
O tipo dessa expressão de "desencapsulamento" é o tipo subjacente do tipo definido pelo usuário. 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

O operador de desencapsulamento não encapsula exatamente uma camada de encapsulamento.
Vários operadores de desencapsulamento podem ser usados para acessar um valor com disposição multiplicada.

Por exemplo:

```qsharp
newtype WrappedInt = Int;
newtype DoublyWrappedInt = WrappedInt;

...
    let x = DoublyWrappedInt(WrappedInt(6));
    let y = x!;       // y is WrappedInt(6)
    let z = x!!;      // z is 6
    let a = x + 5;    // This is an error, a DoublyWrappedInt isn't an Int
    let b = x! + 5;   // Also an error
    let c = x!! + 5;  // This is valid, c will be 11
...
```

Mais detalhes sobre o operador de desencapsulamento podem ser encontrados em [expressões de tipo em Q #](xref:microsoft.quantum.guide.expressions).

### <a name="creating-values-of-user-defined-types"></a>Criando valores de tipos definidos pelo usuário

Os valores de um tipo definido pelo usuário podem ser criados chamando o construtor de tipo correspondente:

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

Como alternativa, novos valores podem ser criados de existentes usando [expressões de copiar e atualizar](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions). Assim como para matrizes, essas expressões copiam todos os valores de item da expressão original, com exceção dos itens nomeados especificados. Para esses valores são definidos como aqueles definidos no lado direito da expressão. Qualquer outra construção de linguagem, como por exemplo, [atualizar e reatribuir instruções](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), que estão disponíveis para itens de matriz existem para itens nomeados em tipos definidos pelo usuário também.

```qsharp
newtype ComplexArray = (Count : Int, Data : Complex[]);

function AsComplexArray (data : Double[]) : ComplexArray {

    mutable res = ComplexArray(0, new Complex[0]);
    for (item in data) {
        set res w/= Data <- res::Data + [Complex(item, 0.)]; // update-and-reassign statement
    }
    return res w/ Count <- Length(res::Data); // returning a copy-and-update expression
}
```

Tipos definidos pelo usuário podem ser usados em qualquer lugar que qualquer outro tipo possa ser usado.
Em particular, é possível definir uma matriz de um tipo definido pelo usuário e incluir um tipo definido pelo usuário como um elemento de um tipo de tupla.

Observação não é possível criar estruturas de tipo recursiva.
Ou seja, o tipo que define um tipo definido pelo usuário pode não ser um tipo de tupla que inclua um elemento do tipo definido pelo usuário.
Em geral, os tipos definidos pelo usuário podem não ter dependências cíclicas entre si, portanto, o seguinte conjunto de definições de tipo seria ilegal:

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```


## <a name="operation-and-function-types"></a>Operação e tipos de função

O tipo básico para qualquer callable é escrito como `('Tinput => 'Tresult)` ou `('Tinput -> 'Tresult)` , onde ambos `'Tinput` e `'Tresult` são tipos.
Eles são chamados de *assinatura* do callable.

Todos os chamadores de Q # são considerados para pegar um único valor como entrada e retornar um único valor como saída.
Os valores de entrada e saída podem ser tuplas.
Chamadores que não têm nenhum retorno de resultado `Unit` .
Os chamadores que não têm nenhuma entrada usam a tupla vazia como entrada.

> [!NOTE]
> O primeiro formulário, com `=>` , é usado para operações; o segundo formulário, com `->` , para funções.
> Por exemplo, `((Qubit, Pauli) => Result)` representa a assinatura de uma possível operação de medição de qubit único.
Os tipos de *função* são completamente especificados por sua assinatura.
Por exemplo, uma função que computa o seno de um ângulo teria tipo `(Double -> Double)` .

*As operações*---, mas não funções---têm determinadas características adicionais que são expressas como parte do tipo de operação. Essas características incluem informações sobre o que *transmissão functors* a operação dá suporte.
Por exemplo, se a execução da operação puder ser condicionada no estado de outros qubits, ela deverá dar suporte a `Controlled` functor; se a operação tiver um inverso, ela deverá dar suporte ao `Adjoint` functor. Transmissão functors e operações são discutidas em detalhes em [operações e funções em Q #](xref:microsoft.quantum.guide.operationsfunctions), mas aqui simplesmente discutimos como isso altera a assinatura da operação.

Para exigir suporte para o `Controlled` e/ou `Adjoint` functor em um tipo de operação, precisamos adicionar uma anotação que indica as características correspondentes.
Uma anotação `is Ctl` (por exemplo, `(Qubit => Unit is Ctl)` ) indica que a operação é controlável---ou seja, é uma condição de execução no estado de outro qubit ou qubits. Da mesma forma, `is Adj` indica que a operação tem um erro; ou simplesmente, pode ser "invertida", de forma que a aplicação sucessiva de uma operação e, em seguida, seu adjacente a um estado deixa o estado inalterado. 

Se quisermos exigir que uma operação desse tipo dê suporte a `Adjoint` e `Controlled` functor, podemos expressar isso como `(Qubit => Unit is Adj + Ctl)` . Por exemplo, a operação Pauli interna <xref:microsoft.quantum.intrinsic.x> tem o tipo `(Qubit => Unit is Adj + Ctl)` . 

Um tipo de operação que não dá suporte a nenhum transmissão functors é especificado por seu tipo de entrada e saída sozinho, sem anotação adicional.

### <a name="type-parameterized-functions-and-operations"></a>Funções e operações com parâmetros de tipo

Tipos chamáveis podem conter parâmetros de tipo.
Os parâmetros de tipo são indicados por um símbolo prefixado por uma aspa simples; por exemplo, `'A` é um parâmetro de tipo legal.
Detalhes sobre a definição de chamadores com parâmetros de tipo são fornecidos nas [operações e funções na página de Q #](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) .

Um parâmetro de tipo pode aparecer mais de uma vez em uma única assinatura.
Por exemplo, uma função que aplica outra função a cada elemento de uma matriz e retorna os resultados coletados teriam assinatura `(('A[], 'A->'A) -> 'A[])` .
Da mesma forma, uma função que retorna a composição de duas operações pode ter assinatura `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .

Ao invocar um callable-parametrizado de tipo, todos os argumentos que têm o mesmo parâmetro de tipo devem ser do mesmo tipo.

O Q # não fornece um mecanismo para restringir os possíveis tipos que podem ser substituídos por um parâmetro de tipo.

## <a name="whats-next"></a>O que vem a seguir?
Agora que você viu todos os tipos que compõem a linguagem Q #, você pode se encabeçar para [digitar expressões em Q #](xref:microsoft.quantum.guide.expressions) para ver como criar e manipular expressões desses vários tipos.


