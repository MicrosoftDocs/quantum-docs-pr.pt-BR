---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Função LeftShiftedI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 3a7220489bfa241e2337df14291bafb1d6e0e19e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209852"
---
# <a name="leftshiftedi-function"></a>Função LeftShiftedI

Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Desloca a representação bit a bit de um número à esquerda por um determinado número de bits.

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a>Entrada

### <a name="value--int"></a>valor: [int](xref:microsoft.quantum.lang-ref.int)

O número cuja representação em bits bit a lado deve ser deslocada para a esquerda (mais significativa).


### <a name="amount--int"></a>valor: [int](xref:microsoft.quantum.lang-ref.int)

O número de bits pelo qual deve `value` ser deslocado para a esquerda.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O valor de `value` , deslocado para a esquerda por `amount` bits.

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```