---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Função IntegerBits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: 3352c1b3003ee387fb03b72461fedb400e29046d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855411"
---
# <a name="integerbits-function"></a>Função IntegerBits

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna todas as posições nas quais os bits de um inteiro são definidos.

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a>Entrada

### <a name="value--int"></a>valor: [int](xref:microsoft.quantum.lang-ref.int)

Um número não negativo.


### <a name="length--int"></a>comprimento: [int](xref:microsoft.quantum.lang-ref.int)

O número de bits na expansão binária de `value` .



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma matriz que contém todas as posições de bits (a partir de 0) que são 1 na expansão binária, `value` Considerando todos os bits até a posição `length - 1` .  Todas as posições são ordenadas na matriz por posição em uma ordem crescente.

## <a name="example"></a>Exemplo

```qsharp
IntegerBits(23, 5); // [0, 1, 2, 4]
IntegerBits(10, 4); // [1, 3]
```