---
uid: Microsoft.Quantum.Canon.BoundA
title: Função bounda
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3132bf198e98dd1a2b433f36b000060e7e721865
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216941"
---
# <a name="bounda-function"></a>Função bounda

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.
O modificador `A` indica que todas as operações na matriz são adjointable.

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a>Entrada

### <a name="operations--t--unit--is-adj"></a>operações: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj []

Uma sequência de operações a ser executada em uma determinada entrada.



## <a name="output--t--unit--is-adj"></a>Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

Uma nova operação que executa cada operação específica em sequência em sua entrada.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O destino no qual cada uma das operações na matriz atua.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)