---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Operação ApplySeriesOfOpsC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: eaa0ea3e33cce708af5879cfbe875397fbb82a8a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217927"
---
# <a name="applyseriesofopsc-operation"></a>Operação ApplySeriesOfOpsC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz. Controlado

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a>Entrada

### <a name="listofops--t--unit--is-ctl"></a>listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL []

Lista de operações, cada uma levando uma matriz não, a ser aplicada. Eles são aplicados em sequência, o índice mais baixo primeiro.
Cada um deve ter um functor controlado


### <a name="targets--int"></a>destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []

Matrizes aninhadas que descrevem os destinos da operação. Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.


### <a name="register--t"></a>registrar: t []

Qubit registrar-se para ser tratado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)