---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: Função LeftShiftedL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 014653011574d0fabb4b9aa04cedf58b87ddf798
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842151"
---
# <a name="leftshiftedl-function"></a>Função LeftShiftedL

Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

```qsharp
let c = a <<< b;
let c = LeftShiftedL(a, b);
```