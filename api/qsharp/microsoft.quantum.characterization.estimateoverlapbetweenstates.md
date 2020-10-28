---
uid: Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates
title: Operação EstimateOverlapBetweenStates
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.
ms.openlocfilehash: 58a367c7ff7d13ac5c1eb1588fb8dac66414776c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693840"
---
# <a name="estimateoverlapbetweenstates-operation"></a>Operação EstimateOverlapBetweenStates

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Agrupa [](https://nuget.org/packages/)


Dadas duas operações que cada uma das cópias de um estado, o estima a sobreposição de quadrado entre os Estados preparados por cada operação.

```qsharp
operation EstimateOverlapBetweenStates (preparation1 : (Qubit[] => Unit is Adj), preparation2 : (Qubit[] => Unit is Adj), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Entrada

### <a name="preparation1--qubit--unit-adj"></a>preparation1: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)

A primeira das duas operações de preparação de estado a ser comparada.


### <a name="preparation2--qubit--unit-adj"></a>preparation2: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)

A segunda das duas operações de preparação de estado a ser comparada.


### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits em que `commonPreparation` , `preparation1` e `preparation2` todos os Act.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

O número de medições a serem usadas para estimar a sobreposição.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Comentários

Esta operação usa o teste de permuta para localizar $ $ \begin{align} \left | \braket{00\cdots 0 | V ^ {\dagger} U | 00 \ cdots 0} \right | ^ 2 \end{Align} $ $, em que $U $ é a representação unitário da ação de `preparation1` e onde $V $ corresponde a `preparation2` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Caracterization. EstimateRealOverlapBetweenStates](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [Microsoft. Quantum. Caracterization. EstimateImagOverlapBetweenStates](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)