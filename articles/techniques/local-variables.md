---
title: 'Variáveis locais-Q # técnicas | Microsoft Docs'
description: 'Variáveis locais – técnicas de Q #'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.local-variables
ms.openlocfilehash: 8b1de5c096210fb36a81c127a8bbbe1b39522741
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820174"
---
# <a name="local-variables"></a>Variáveis locais #

Um valor de qualquer tipo em Q # pode ser atribuído a uma variável para reutilização em uma operação ou função usando a palavra-chave `let`.
Por exemplo:

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

Isso atribui uma determinada matriz de operadores de Pauli a uma variável chamada `measurementOperator`.

> [!TIP]
> Observe que não precisamos especificar explicitamente o tipo da nossa nova variável, pois a expressão no lado direito da instrução de `let` não é ambígua e o tipo é inferido pelo compilador. 

As variáveis em Q # são *imutáveis*, o que significa que, depois que uma variável tiver sido definida dessa forma, ela não poderá mais ser alterada de forma alguma.
Isso permite várias otimizações úteis, incluindo a otimização da lógica clássica que atua em variáveis a serem reordenadas para aplicar a `Adjoint` variante de uma operação.

As variáveis definidas usando a associação de `let` como acima são locais para um escopo específico, como o corpo de uma operação ou o conteúdo de um loop de `for`.


## <a name="mutability"></a>Imutabilidade ##

Como uma alternativa para criar uma variável com `let`, a palavra-chave `mutable` criará uma variável mutável especial que pode ser reassociada após ser criada inicialmente usando a palavra-chave `set`.

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {
    mutable samples = new Int[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}
```

Todos os tipos em Q #, incluindo matrizes, seguem a semântica de valor. Em particular, não é possível atualizar itens de matriz. Para modificar uma matriz existente, é necessário aproveitar um mecanismo de cópia e atualização como aquele para registros no F#. Usando as ferramentas de biblioteca para matrizes fornecidas no [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), podemos, por exemplo, definir facilmente uma função que retorna uma matriz de Paulis em que o Pauli no índice `i` usa o valor determinado e todas as outras entradas são a identidade: 

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    
    let arr = ConstantArray(n, PauliI); // creates an array of filled with PauliI
    return arr w/ i <- pauli; // constructs a new array based on arr except that entry i is set to pauli
}
```

Falaremos mais sobre como trabalhar com matrizes ao abordar as instruções e expressões de Q #. 

A imutabilidade em Q # é um conceito que se aplica a um *símbolo* em vez de um tipo ou valor. Especificamente, ele não tem uma representação no sistema de tipos, implicitamente ou explicitamente, e se uma associação é mutável (conforme indicado pela palavra-chave `mutable`) ou imutável (conforme indicado pelo `let`) não altera o tipo de variável (s) associada. Isso fornece uma maneira importante de isolar a imutabilidade dentro de funções e operações especializadas.
Em particular, embora uma especialização adjacente para uma operação que usa uma variável mutável não possa ser gerada automaticamente, a geração automática funciona bem para uma operação que chama uma função que usa a imutabilidade.
Por esse motivo, é uma boa prática fazer funções e operações que usam a imutabilidade o mais curto possível e compacto possível, para que o restante do programa Quantum possa ser escrito usando variáveis imutáveis comuns.


## <a name="deconstruction"></a>Desconstrução ##

Além de atribuir uma única variável, as palavras-chave `let` e `mutable`-ou na verdade qualquer outra construção de associação-também permite desempacotar o conteúdo de um [tipo de tupla](xref:microsoft.quantum.language.type-model#tuple-types).
Uma atribuição desse formulário é mencionada para *desconstruir* os elementos dessa tupla.
Por exemplo, se modelarmos um termo em um Hamiltonian por uma tupla, podemos usar a desconstrução para acessar os dados diferentes que precisamos simular sob esse termo:

```qsharp
// Represents H = 3.1 X_0 Z_1.
let (_, (paulis, idxQubits)) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // paulis and idxQubits are both immutable variables
mutable ((c1, c2), _) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // c1 and c2 are both mutable variables
```


