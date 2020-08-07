---
title: Tipos emQ#
description: Saiba mais sobre os diferentes tipos usados na Q# linguagem de programação.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
no-loc:
- Q#
- $$v
ms.openlocfilehash: b034af0b1d3b967b5680403341813407e4412f93
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869589"
---
# <a name="types-in-no-locq"></a>Tipos emQ#

Este artigo descreve o Q# modelo de tipo e a sintaxe para especificar e trabalhar com tipos. Para obter detalhes sobre como criar e operar em expressões desses tipos, consulte [expressões de tipo](xref:microsoft.quantum.guide.expressions).

Observe que Q# é uma linguagem *fortemente tipada* , de modo que o uso cuidadoso desses tipos pode ajudar o compilador a fornecer fortes garantias sobre os Q# programas em tempo de compilação.
Para fornecer as garantias mais fortes possíveis, as conversões entre os tipos no Q# devem ser explícitas usando chamadas para funções que expressam essa conversão. 
Q#fornece uma variedade de funções desse tipo como parte do <xref:microsoft.quantum.convert> namespace.
Por outro lado, os upcasts para tipos compatíveis ocorrem implicitamente. 

Q#fornece os dois tipos primitivos, que são usados diretamente e várias maneiras de produzir novos tipos de outros tipos.
Descrevemos cada um no restante deste artigo.

## <a name="primitive-types"></a>Tipos primitivos

A Q# linguagem fornece os seguintes *tipos primitivos*, todos os quais você pode usar diretamente em Q# programas. Você também pode usar esses tipos primitivos para construir novos tipos.

- O `Int` tipo representa um inteiro com sinal de 64 bits, por exemplo,,, `2` `107` `-5` .
- O `BigInt` tipo representa um inteiro assinado de tamanho arbitrário, por exemplo,,, `2L` `107L` `-5L` .
   Esse tipo é baseado no .NET<xref:System.Numerics.BigInteger>
   Escreva.

- O `Double` tipo representa um número de ponto flutuante de precisão dupla, por exemplo,,, `0.0` `-1.3` `4e-7` .
- O `Bool` tipo representa um valor booliano de `true` ou `false` .
- O `Range` tipo representa uma sequência de números inteiros, indicados por `start..step..stop` , em que a denotação da etapa é opcional. 
   Por exemplo, `start .. stop` corresponde a `start..1..stop` e `1..2..7` representa a sequência $ \{ 1, 3, 5, 7 \} $.
- O `String` tipo é uma sequência de caracteres Unicode que é opaca para o usuário depois de criado.
  Use o `string` tipo para relatar mensagens para um host clássico no caso de um erro ou evento de diagnóstico.
- O `Unit` tipo pode ter apenas um valor, `()` . 
  Use esse tipo para indicar que uma Q# função ou operação não retorna nenhuma informação. 
- O `Qubit` tipo representa um bit quântico ou qubit.
   `Qubit`os s são opacos para o usuário. A única operação possível com eles, além de passá-los para outra operação, é testar a identidade (igualdade).
   Por fim, você implementa ações em `Qubit` s chamando instruções intrínsecas em um processador Quantum (ou um simulador Quantum).
- O `Pauli` tipo representa um dos quatro operadores de Pauli de qubit único.
   Use esse tipo para indicar a operação base para rotações e para especificar o observável que está sendo medido.
   É um tipo enumerado que tem quatro valores possíveis: `PauliI` ,, `PauliX` `PauliY` e `PauliZ` , que são constantes do tipo `Pauli` .
- O `Result` tipo representa o resultado de uma medida.
   É um tipo enumerado com dois valores possíveis: `One` e `Zero` , que são constantes do tipo `Result` .
   `Zero`indica que a eigenvalue + 1 foi medida; `One`indica que-1 eigenvalue foi medido.

As constantes,,,,,, `true` `false` `PauliI` `PauliX` `PauliY` `PauliZ` `One` e `Zero` são todos os símbolos reservados no Q# .

## <a name="array-types"></a>Tipos de matriz

* Para qualquer Q# tipo válido, há um tipo que representa uma matriz de valores desse tipo.
    Por exemplo, `Qubit[]` e `(Bool, Pauli)[]` representam matrizes de `Qubit` valores e `(Bool, Pauli)` valores de tupla.

* Uma matriz de matrizes também é válida. Expandindo no exemplo anterior, uma matriz de `(Bool, Pauli)` matrizes é denotada `(Bool, Pauli)[][]` .

> [!NOTE] 
> Este exemplo, `(Bool, Pauli)[][]` , representa uma matriz potencialmente irregular de matrizes e não uma matriz bidimensional retangular. Q#não oferece suporte a matrizes multidimensionais retangulares.

* Um valor de matriz pode ser escrito no Q# código-fonte usando colchetes em volta dos elementos de uma matriz, como em `[PauliI, PauliX, PauliY, PauliZ]` .
O tipo de base comum de todos os itens na matriz determina o tipo de um literal de matriz. Portanto, construir uma matriz com elementos que não têm nenhum tipo base comum gera um erro.  
Para obter um exemplo, consulte [matrizes de callablefiles](xref:microsoft.quantum.guide.expressions#arrays-of-callables).

    > [!WARNING]
    > Depois de criados, os elementos de uma matriz não podem ser alterados.
    > Para construir uma matriz modificada, use as [instruções UPDATE-and-REASSIGN](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) ou as [expressões Copy-and-Update](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).

* Como alternativa, uma matriz pode ser criada com base em seu tamanho usando a `new` palavra-chave:

    ```qsharp
    let zeros = new Int[13];
    // you can also use new for creating empty arrays:
    let emptyRegister = new Qubit[0];
    ```

* Use a função principal `Length` para obter o número de elementos de uma matriz como um `Int` .
* Matrizes podem ser inscrições para obter um único elemento ou novas matrizes que contenham um subconjunto dos elementos de uma matriz.
Os subscritos das matrizes são baseados em zero e devem ser do tipo `Int` ou tipo `Range` :

    ```qsharp
    let arr = [10, 11, 36, 49];
    let ten = arr[0]; // 10
    let odds = arr[1..2..4]; // [11, 49]
    ```

## <a name="tuple-types"></a>Tipos de tupla

As tuplas são um conceito poderoso usado em todo Q# o mundo para coletar valores juntos em um único valor, facilitando sua passagem.
Em particular, usando a notação de tupla, você pode expressar que cada operação e que pode ser chamado leva exatamente uma entrada e retorna exatamente uma saída.

* Dado zero ou mais tipos diferentes `T0` , `T1` ,..., `Tn` você pode indicar um novo *tipo de tupla* como `(T0, T1, ..., Tn)` .
Os tipos usados para construir um novo tipo de tupla podem ser tuplas, como em `(Int, (Qubit, Qubit))` .
No entanto, esse aninhamento é sempre finito, pois os tipos de tupla não podem, sob nenhuma circunstância, conter.

* Os valores do novo tipo de tupla são tuplas formadas por sequências de valores de cada tipo na tupla.
Por exemplo, `(3, false)` é uma tupla cujo tipo é o tipo de tupla `(Int, Bool)` .
É possível criar matrizes de tuplas, tuplas de matrizes, tuplas de subtuplas e assim por diante.

* A partir de Q# 0,3, `Unit` é o nome do *tipo* da tupla vazia; `()` é usado para o *valor* da tupla vazia.

* As instâncias de tupla são imutáveis.
Q#não fornece um mecanismo para alterar o conteúdo de uma tupla depois de criada.



### <a name="singleton-tuple-equivalence"></a>Equivalência de tupla singleton

É possível criar uma tupla singleton (elemento único) `('T1)` , como `(5)` ou `([1,2,3])` .
No entanto, Q# trata uma tupla singleton como equivalente a um valor do tipo incluído.
Ou seja, não há nenhuma diferença entre `5` e `(5)` , ou entre `5` e `(((5)))` , ou entre `(5, (6))` e `(5, 6)` .
Ele é tão válido para gravar `(5)+3` como é para gravação `5+3` ; as duas expressões são avaliadas como `8` .

Essa equivalência aplica-se a todas as finalidades, incluindo atribuições e expressões.
Dada qualquer expressão, a mesma expressão entre parênteses é uma expressão do mesmo tipo.
Por exemplo, `(7)` é uma expressão do tipo `Int` , `([1,2,3])` é uma expressão do tipo `Int[]` e `((1,2))` é uma expressão do tipo `(Int, Int)` .

Em particular, isso significa que você pode exibir uma operação ou função cuja tupla de entrada ou tipo de tupla de saída tem um campo como pegar um único argumento ou retornar um único valor.

Nós nos referimos a essa propriedade como _equivalência de tupla singleton_.


## <a name="user-defined-types"></a>Tipos definidos pelo usuário

Uma declaração de tipo definida pelo usuário consiste na palavra-chave `newtype` , seguida pelo nome do tipo definido pelo usuário, uma `=` especificação de tipo válida e um ponto-e-vírgula de terminação.

Por exemplo:

```qsharp
newtype PairOfInts = (Int, Int);
```
    
* Cada Q# arquivo de origem pode declarar qualquer número de tipos definidos pelo usuário.
* Os nomes de tipo devem ser exclusivos em um namespace e podem não entrar em conflito com os nomes de operação e de função.
* Os tipos definidos pelo usuário são distintos, mesmo que os tipos base sejam idênticos.
Em particular, não há conversão automática entre os valores de dois tipos definidos pelo usuário, mesmo que os tipos subjacentes sejam idênticos.

### <a name="named-vs-anonymous-items"></a>Itens nomeados vs. anônimos

Um Q# arquivo pode definir um novo tipo nomeado contendo um único valor de qualquer tipo legal.
Para qualquer tipo de tupla `T` , você pode declarar um novo tipo definido pelo usuário que seja um subtipo de `T` com a `newtype` instrução.
No @"microsoft.quantum.math" namespace, por exemplo, números complexos são definidos como um tipo definido pelo usuário:

```qsharp
newtype Complex = (Double, Double);
```
Essa instrução cria um novo tipo com dois itens anônimos do tipo `Double` .   

Além de itens anônimos, os tipos definidos pelo usuário também dão suporte a *itens nomeados* a partir da Q# versão 0,7 ou superior. Por exemplo, você pode nomear os itens para `Re` para o duplo que representa a parte real de um número complexo e `Im` para a parte imaginária: 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Nomear um item em um tipo definido pelo usuário não significa que todos os itens precisam ser nomeados-qualquer combinação de itens nomeados e sem nome é suportada. Além disso, os itens internos também podem ser nomeados.
O tipo `Nested` , conforme definido abaixo, por exemplo, tem um tipo subjacente `(Double, (Int, String))` , do qual apenas o item do tipo `Int` é nomeado e todos os outros itens são anônimos. 

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

Embora ambos `Complex` `Polar` tenham um tipo subjacente `(Double, Double)` , os dois tipos são totalmente incompatíveis no Q# , minimizando o risco de chamar acidentalmente uma função matemática complexa com coordenadas polares e vice-versa.

#### <a name="access-anonymous-items-with-the-unwrap-operator"></a>Acessar itens anônimos com o operador de desencapsulamento

Para acessar itens anônimos, primeiro extraia o valor encapsulado usando o operador de sufixo `!` .
Com o operador "sem encapsulamento", `!` você pode extrair o valor contido em um tipo definido pelo usuário.
O tipo dessa expressão de "desencapsulamento" é o tipo subjacente do tipo definido pelo usuário. 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

Um único operador de desencapsulamento desencapsula uma camada de encapsulamento. Use vários operadores de desencapsulamento para acessar um valor com disposição multiplicada.

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

Para obter mais detalhes sobre o operador de desencapsulamento, consulte [expressões de tipo em Q# ](xref:microsoft.quantum.guide.expressions).

### <a name="creating-values-of-user-defined-types"></a>Criando valores de tipos definidos pelo usuário

Crie valores de um tipo definido pelo usuário chamando o construtor de tipo correspondente:

```qsharp
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

Como alternativa, você pode criar novos valores de existentes usando [expressões de copiar e atualizar](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions). Assim como acontece com matrizes, as expressões Copy-and-Update copiam todos os valores de item da expressão original, exceto os itens nomeados especificados. Para essas exceções, os valores desses itens são os valores definidos no lado direito da expressão. Qualquer outra construção de linguagem que esteja disponível para itens de matriz, por exemplo, [atualizar e reatribuir instruções](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), existir para itens nomeados em tipos definidos pelo usuário também.

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

* Você pode usar tipos definidos pelo usuário em qualquer lugar em que usar qualquer outro tipo.
Em particular, é possível definir uma matriz de um tipo definido pelo usuário e incluir um tipo definido pelo usuário como um elemento de um tipo de tupla.

* Não é possível criar estruturas de tipo recursiva.
Ou seja, o tipo que define um tipo definido pelo usuário não pode ser um tipo de tupla que inclua um elemento do tipo definido pelo usuário.
Em geral, os tipos definidos pelo usuário podem não ter dependências cíclicas entre si, portanto, o seguinte conjunto de definições de tipo é inválido:

    ```qsharp
    newtype TypeA = (Int, TypeB);
    newtype TypeB = (Double, TypeC);
    newtype TypeC = (TypeA, Range);
    ```


## <a name="operation-and-function-types"></a>Operação e tipos de função

Considerando os tipos `'Tinput` e `'Tresult` :

* `('Tinput => 'Tresult)`é o tipo básico para qualquer *operação*, por exemplo `((Qubit, Pauli) => Result)` .
* `('Tinput -> 'Tresult)`é o tipo básico para qualquer *função*, por exemplo `(Int -> Int)` . 

Eles são chamados de *assinatura* do callable.

* Todos os Q# chamados usam um único valor como entrada e retornam um único valor como saída.
* Você pode usar tuplas para os valores de entrada e saída.
* Chamadores que não têm resultado, retornam `Unit` .
* Os chamadores que não têm nenhuma entrada usam a tupla vazia como entrada.

### <a name="functors"></a>Transmissão functors

Os tipos de *função* são completamente especificados por sua assinatura. Por exemplo, uma função que computa o seno de um ângulo teria tipo `(Double -> Double)` . 

*As operações* têm determinadas características adicionais que são expressas como parte do tipo de operação. Essas características incluem informações sobre a qual *transmissão functors* a operação dá suporte.
Por exemplo, se a execução da operação depender do estado de outros qubits, ela deverá dar suporte a `Controlled` functor; se a operação tiver um inverso, ela deverá dar suporte ao `Adjoint` functor.

> [!NOTE]
> Este artigo aborda apenas como transmissão functors a alteração da assinatura de operação. Para obter mais detalhes sobre transmissão functors e operações, consulte [operações e funções Q# no ](xref:microsoft.quantum.guide.operationsfunctions). 

Para exigir suporte para o `Controlled` e/ou `Adjoint` functor em um tipo de operação, você precisa adicionar uma anotação que indica as características correspondentes.
A anotação `is Ctl` (por exemplo, `(Qubit => Unit is Ctl)` ) indica que a operação é controlável. Ou seja, sua execução depende do estado de outro qubit ou qubits. Da mesma forma, a anotação `is Adj` indica que a operação tem um erro, ou seja, pode ser "invertida", de forma que a aplicação sucessiva de uma operação e, em seguida, o estado adjacente a um State deixa o estado inalterado. 

Se você quiser exigir que uma operação desse tipo dê suporte a `Adjoint` e functor, `Controlled` você pode expressar isso como `(Qubit => Unit is Adj + Ctl)` . Por exemplo, a operação Pauli interna <xref:microsoft.quantum.intrinsic.x> tem o tipo `(Qubit => Unit is Adj + Ctl)` . 

Um tipo de operação que não dá suporte a nenhum transmissão functors é especificado por seu tipo de entrada e saída sozinho, sem anotação adicional.

### <a name="type-parameterized-functions-and-operations"></a>Funções e operações com parâmetros de tipo

Tipos chamáveis podem conter *parâmetros de tipo*.
Use um símbolo prefixado por uma aspa simples para indicar um parâmetro de tipo; por exemplo, `'A` é um parâmetro de tipo legal.
Para obter mais informações e detalhes sobre como definir os chamadores com parâmetros de tipo, consulte [operações e funções Q# no ](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables).

Um parâmetro de tipo pode aparecer mais de uma vez em uma única assinatura.
Por exemplo, uma função que aplica outra função a cada elemento de uma matriz e retorna os resultados coletados tem a assinatura `(('A[], 'A->'A) -> 'A[])` .
Da mesma forma, uma função que retorna a composição de duas operações tem a assinatura `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .

Quando você invoca um callable-parametrizado de tipo, todos os argumentos que têm o mesmo parâmetro de tipo devem ser do mesmo tipo.

Q#não fornece um mecanismo para restringir os possíveis tipos que um usuário pode substituir por um parâmetro de tipo.

## <a name="next-steps"></a>Próximas etapas

Agora que você viu todos os tipos que compõem a Q# linguagem, consulte [expressões de tipo no Q# ](xref:microsoft.quantum.guide.expressions) para saber como criar e manipular expressões desses vários tipos.
