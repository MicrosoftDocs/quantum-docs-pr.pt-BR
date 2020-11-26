---
uid: Microsoft.Quantum.Simulation.TrotterStep
title: Função TrotterStep
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStep
qsharp.summary: Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.
ms.openlocfilehash: 516b40ac9920a4a8acc09ad7f558db88dbeb41e8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192801"
---
# <a name="trotterstep-function"></a>Função TrotterStep

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementa uma única etapa de tempo de evolução de tempo pelo sistema descrito em um `EvolutionGenerator` usando uma decomposição Trotter – Suzuki.

```qsharp
function TrotterStep (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, trotterOrder : Int, trotterStepSize : Double) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="evolutiongenerator--evolutiongenerator"></a>evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Uma descrição completa do sistema a ser simulado.


### <a name="trotterorder--int"></a>trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)

Ordem do integrador Trotter. Deve ser 1 ou um número par.


### <a name="trotterstepsize--double"></a>trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)

Duração da evolução de tempo simulada em uma única etapa de Trotter.



## <a name="output--qubit--unit--is-adj--ctl"></a>Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

Operação unitário que aproxima uma única etapa da evolução do tempo para duração `trotterStepSize` .

## <a name="remarks"></a>Comentários

Para obter mais informações sobre a decomposição Trotter – Suzuki, consulte [composição de tempo ordenado](/quantum/libraries/control-flow#time-ordered-composition).