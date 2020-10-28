---
title: Variáveis em Q#
description: Saiba como trabalhar com variáveis diferentes em Q#
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
no-loc:
- Q#
- $$v
ms.openlocfilehash: 67c71c09e004d77360902360fefc7a7752e4a829
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690928"
---
# <a name="variables-in-no-locq"></a>Variáveis em Q#

Q# distingue entre símbolos mutáveis e imutáveis, ou *variáveis* , que são associados/atribuídos a expressões.
Em geral, o uso de símbolos imutáveis é incentivado porque permite que o compilador execute mais otimizações.

O lado esquerdo de uma associação consiste em uma tupla de símbolos e no lado direito de uma expressão.

## <a name="immutable-variables"></a>Variáveis imutáveis

Você pode atribuir um valor de qualquer tipo em Q# uma variável para reutilização em uma operação ou função usando a `let` palavra-chave. 

Uma associação imutável consiste na palavra-chave `let` , seguida por uma tupla de símbolo ou símbolo, um sinal de igual `=` , uma expressão para associar os símbolos a e um ponto e vírgula de terminação.

Por exemplo:

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

Isso atribui uma determinada matriz de operadores Pauli ao nome da variável (ou "Symbol"), `measurementOperator` .

> [!NOTE]
> No exemplo anterior, não é necessário especificar explicitamente o tipo da nova variável, uma vez que a expressão no lado direito da `let` instrução não é ambígua e o compilador infere o tipo correto. 

As variáveis definidas usando `let` são *imutáveis* , o que significa que, uma vez definida, você não poderá mais alterá-la de qualquer forma.
Isso permite várias otimizações úteis, incluindo a otimização da lógica clássica que atua em variáveis a serem reordenadas para aplicar a `Adjoint` variante de uma operação.

## <a name="mutable-variables"></a>Variáveis mutáveis

Como alternativa à criação de uma variável com `let` , a `mutable` palavra-chave cria uma variável mutável que *pode* ser reassociada depois de ser inicialmente criada usando `set` -se a palavra-chave.

Você pode reassociar símbolos declarados e associados como parte de uma `mutable` instrução a um valor diferente posteriormente no código. Se um símbolo for reassociado mais tarde no código, seu tipo não será alterado e o valor vinculado recentemente deverá ser compatível com esse tipo.

### <a name="rebinding-of-mutable-symbols"></a>Reassociação de símbolos mutáveis

Você pode reassociar uma variável mutável usando uma `set` instrução.
Essa reassociação consiste na palavra-chave `set` , seguida por uma tupla de símbolo ou símbolo, um sinal de igual `=` , uma expressão para reassociar os símbolos a e um ponto e vírgula de terminação.

Veja a seguir alguns exemplos de técnicas de instrução de reassociação.

#### <a name="apply-and-reassign-statements"></a>Instruções de aplicar e reatribuir

Um determinado tipo de `set` instrução, a instrução *Apply-e-REASSIGN* , fornece uma maneira conveniente de concatenação se o lado direito consistir no aplicativo de um operador binário e o resultado for ser reassociado ao argumento esquerdo para o operador. Por exemplo,

```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
incrementa o valor do contador `counter` em cada iteração do `for` loop. O código anterior é equivalente a 

```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

Instruções semelhantes estão disponíveis para todos os operadores binários nos quais o tipo do lado esquerdo corresponde ao tipo de expressão. Essas instruções fornecem uma maneira conveniente de acumular valores.

Por exemplo, suponhamos `qubits` é um registro de qubits:
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

#### <a name="update-and-reassign-statements"></a>Instruções UPDATE-and-REASSIGN

Existe uma concatenação semelhante para [expressões de copiar e atualizar](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) no lado direito.
De modo correspondente, as instruções *Update-and-REASSIGN* existem para *itens nomeados* em tipos definidos pelo usuário, bem como para *itens de matriz* .  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function ComplexSum(reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

No caso de matrizes, [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) na Q# biblioteca Standard fornece as ferramentas necessárias para muitas necessidades comuns de inicialização e manipulação de matriz e, portanto, ajuda a evitar a necessidade de atualizar itens de matriz em primeiro lugar. 

As instruções UPDATE-and-REASSIGN fornecem uma alternativa, se necessário:

```qsharp
operation GenerateRandomInts(max : Int, nSamples : Int) : Int[] {
    mutable samples = new Double[0];
    for (i in 1 .. nSamples) {
        set samples += [RandomInt(max)];
    }
    return samples;
}

operation SampleUniformDistrbution(nSamples : Int, nSteps : Int) : Double[] {
    let normalization = 1. / IntAsDouble(nSteps);
    mutable samples = GenerateRandomInts(nSteps, nSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

Usando as ferramentas de biblioteca para matrizes fornecidas no [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) , você pode, por exemplo, definir facilmente uma função que retorna uma matriz de `Pauli` tipos em que o elemento no índice `i` usa um determinado `Pauli` valor e todas as outras entradas são a identidade ( `PauliI` ).

Aqui estão duas definições dessa função, com a segunda aproveitando as ferramentas em nossa disposição.

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli if index==location and PauliI if not
    }    
    return pauliArray;
}
```

Em vez de iterar em cada índice na matriz e defini-la condicionalmente como `PauliI` ou no dado `pauli` , você pode usar `ConstantArray` de [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) para criar uma matriz de `PauliI` tipos e, em seguida, simplesmente retornar uma expressão de copiar e atualizar na qual você alterou o valor específico no índice `location` :

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a>Desconstrução de tupla

Além de atribuir uma única variável, você pode usar as `let` `mutable` palavras-chave e-ou qualquer outra construção de associação, como `set` -para desempacotar o conteúdo de um [tipo de tupla](xref:microsoft.quantum.guide.types#tuple-types).
Uma atribuição desse formulário é mencionada para *desconstruir* os elementos dessa tupla.

Se o lado direito da associação for uma tupla, você poderá desconstruir essa tupla após a atribuição.
Essas desconstruções podem envolver tuplas aninhadas e qualquer desconstrução completa ou parcial é válida, desde que a forma da tupla no lado direito seja compatível com a forma da tupla de símbolos.

Por exemplo:

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a>Escopos de associação

Em geral, as ligações de símbolo saem do escopo e se tornam inoperantes no final do bloco de instrução em que ocorrem.
Há duas exceções a essa regra:

- A associação da variável loop de um `for` loop está no escopo do corpo do loop for, mas não após o final do loop.
- Todas as três partes de um `repeat` / `until` loop (o corpo, o teste e a correção) atuam como um único escopo, de modo que os símbolos associados ao corpo estão disponíveis no teste e na correção.

Para ambos os tipos de loops, cada passagem do loop é executado em seu próprio escopo, portanto, as associações de uma passagem anterior não estarão disponíveis em uma passagem posterior.
Para obter mais informações sobre esses loops, consulte [fluxo de controle](xref:microsoft.quantum.guide.controlflow).

Blocos internos herdam associações de símbolo de blocos externos.
Você só pode associar um símbolo uma vez por bloco; é ilegal definir um símbolo com o mesmo nome de outro símbolo que está dentro do escopo (sem "sombreamento").
As seguintes sequências são legais:

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

e

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
...                 // n is not bound to a value
```

Mas isso seria ilegal:

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

como seria:

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="next-steps"></a>Próximas etapas

Saiba mais sobre como [trabalhar com o qubits](xref:microsoft.quantum.guide.qubits) no Q# .