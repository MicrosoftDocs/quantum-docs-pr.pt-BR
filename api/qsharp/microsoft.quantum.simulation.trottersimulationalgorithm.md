---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithm
title: Função TrotterSimulationAlgorithm
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithm
qsharp.summary: '`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.'
ms.openlocfilehash: aa8338ab359441765db72a12f84a3a51e5bee3ce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192529"
---
# <a name="trottersimulationalgorithm-function"></a>Função TrotterSimulationAlgorithm

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


`SimulationAlgorithm` função que usa uma decomposição Trotter – Suzuki para aproximar o operador de tempo-evolução _exp (-IHT)_.

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a>Entrada

### <a name="trotterstepsize--double"></a>trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)

Duração da evolução de tempo simulada em uma única etapa de Trotter.


### <a name="trotterorder--int"></a>trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)

Ordem do integrador Trotter. Deve ser 1 ou um número par.



## <a name="output--simulationalgorithm"></a>Saída: [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)

Um tipo `SimulationAlgorithm`.