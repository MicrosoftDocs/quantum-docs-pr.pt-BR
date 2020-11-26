---
uid: Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates
title: Operação EstimateImagOverlapBetweenStates
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateImagOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the imaginary part of the overlap between the states prepared by each operation.
ms.openlocfilehash: b192abc4ba37d126bf46f94c66cb87fe3bbec4c8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216193"
---
# <a name="estimateimagoverlapbetweenstates-operation"></a>Operação EstimateImagOverlapBetweenStates

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Considerando-se duas operações que cada uma das cópias de um estado, o estima a parte imaginário da sobreposição entre os Estados preparados por cada operação.

```qsharp
operation EstimateImagOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Entrada

### <a name="commonpreparation--qubit--unit--is-adj"></a>commonPreparation: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj

Uma operação que prepara um estado de entrada fixo.


### <a name="preparation1--qubit--unit--is-adj--ctl"></a>preparation1: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

A primeira das duas operações de preparação de estado a ser comparada.


### <a name="preparation2--qubit--unit--is-adj--ctl"></a>preparation2: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

A segunda das duas operações de preparação de estado a ser comparada.


### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits em que `commonPreparation` , `preparation1` e `preparation2` todos os Act.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

O número de medições a serem usadas para estimar a sobreposição.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Comentários

Esta operação usa o teste Hadamard para encontrar a parte imaginária de $ $ \begin{align} \braket{\psi | V ^ {\dagger} U | \psi} \end{Align} $ $, em que $ \ket{\psi} $ é o estado preparado pelo `commonPreparation` , $U $ é a representação unitário da ação de `preparation1` e onde $V $ corresponde a `preparation2` .

## <a name="references"></a>Referências

- Aharonov *et al.* [Quant-pH/0511096](https://arxiv.org/abs/quant-ph/0511096).

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Caracterization. EstimateRealOverlapBetweenStates](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [Microsoft. Quantum. Caracterization. EstimateOverlapBetweenStates](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)