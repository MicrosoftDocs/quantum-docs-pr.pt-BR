---
uid: Microsoft.Quantum.Canon.BoundC
title: Função BoundC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 04dca4ff317bf3cee053f7c3903112f4e05a3973
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694079"
---
# <a name="boundc-function"></a>Função BoundC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.
O modificador `C` indica que todas as operações na matriz são controláveis.

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="operations--t--unit-ctl"></a>operações: não => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) []

Uma sequência de operações a ser executada em uma determinada entrada.



## <a name="output--t--unit-ctl"></a>Saída: t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma nova operação que executa cada operação específica em sequência em sua entrada.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O destino no qual cada uma das operações na matriz atua.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)