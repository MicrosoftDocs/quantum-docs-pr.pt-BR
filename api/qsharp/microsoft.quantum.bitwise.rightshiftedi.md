---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Função RightShiftedI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 5c3106eb73178554184cbfb37333c027805c69f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845250"
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

```qsharp
let c = a >>> b;
let c = RightShiftedI(a, b);
```