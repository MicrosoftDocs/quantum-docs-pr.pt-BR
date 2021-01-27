---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Operação ApplySeriesOfOpsCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9a1f6189428b086c38b1d0f289afb18c2cf1be40
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850864"
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



## <a name="example"></a>Exemplo

O seguinte aplica-se exp ([PauliX, PauliY], 0,5) a qubits 0, 1//then X para qubit 2 Let Ops = [exp ([PauliX, PauliY], 0,5, _), ApplyToFirstQubitCA (X, _)]; permitir índices = [[0, 1], [2]]; ApplySeriesOfOpsCA (Ops, índices, qubitArray);

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)