---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: Função LeftShiftedL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 17e5c845755f74e9703381bc82bfd63be836d038
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694370"
---
# <a name="leftshiftedl-function"></a>Função LeftShiftedL

Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)

Agrupa [](https://nuget.org/packages/)


Desloca a representação bit a bit de um número à esquerda por um determinado número de bits.

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a>Entrada

### <a name="value--bigint"></a>valor: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O número cuja representação em bits bit a lado deve ser deslocada para a esquerda (mais significativa).


### <a name="amount--int"></a>valor: [int](xref:microsoft.quantum.lang-ref.int)

O número de bits pelo qual deve `value` ser deslocado para a esquerda.



## <a name="output--bigint"></a>Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O valor de `value` , deslocado para a esquerda por `amount` bits.

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```Q#
let c = a <<< b;
let c = LeftShiftedL(a, b);
```