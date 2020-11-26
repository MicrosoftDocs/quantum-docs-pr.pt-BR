---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Função RightShiftedI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b20a4a8c281a470af9a4828f8a5ca905a7918723
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209767"
---
# <a name="rightshiftedi-function"></a>Função RightShiftedI

Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Desloca a representação bit a bit de um número à direita por um determinado número de bits.

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a>Entrada

### <a name="value--int"></a>valor: [int](xref:microsoft.quantum.lang-ref.int)

O número cuja representação em bits bit a lado deve ser deslocada para a direita (menos significativa).


### <a name="amount--int"></a>valor: [int](xref:microsoft.quantum.lang-ref.int)

O número de bits pelo qual deve `value` ser deslocado para a direita.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O valor de `value` , deslocado para a direita por `amount` bits.

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```