---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Função IntegerBits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: ab459cd841cdac116cf0e98c094834f628b6a2d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694572"
---
# <a name="integerbits-function"></a>Função IntegerBits

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Agrupa [](https://nuget.org/packages/)


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