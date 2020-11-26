---
uid: Microsoft.Quantum.Canon.BoundCA
title: Função BoundCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: 774a6f57566dce75b98290a7e81540b28afea1af
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216873"
---
# <a name="boundca-function"></a>Função BoundCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.
O modificador `CA` indica que todas as operações na matriz são de adjointable e controláveis.

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="operations--t--unit--is-adj--ctl"></a>operações: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL []

Uma sequência de operações a ser executada em uma determinada entrada.



## <a name="output--t--unit--is-adj--ctl"></a>Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

Uma nova operação que executa cada operação específica em sequência em sua entrada.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O destino no qual cada uma das operações na matriz atua.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)