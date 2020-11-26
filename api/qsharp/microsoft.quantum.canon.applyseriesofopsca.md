---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Operação ApplySeriesOfOpsCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9dd1343b3ebcc75592441f150eee822cfe83f9a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217876"
---
# <a name="applyseriesofopsca-operation"></a>Operação ApplySeriesOfOpsCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz. (Adjacente + controlado)

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="listofops--t--unit--is-adj--ctl"></a>listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL []

Lista de operações, cada uma levando uma matriz não, a ser aplicada. Eles são aplicados em sequência, o índice mais baixo primeiro.
Cada um deve ter um functor controlado e um de controle.


### <a name="targets--int"></a>destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []

Matrizes aninhadas que descrevem os destinos da operação. Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.


### <a name="register--t"></a>registrar: t []

Qubit registrar-se para ser tratado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)