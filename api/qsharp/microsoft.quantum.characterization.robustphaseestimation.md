---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: Operação RobustPhaseEstimation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: 4b37c8275a5b2aee8534bacc5831281aa498b57d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851793"
---
# <a name="robustphaseestimation-operation"></a>Operação RobustPhaseEstimation

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa o algoritmo de estimativa de fase de Quantum não iterativa robusto para um determinado Oracle `U` e eigenstate e fornece uma única estimativa de valor real da fase com dimensionamento de variação no limite de Heisenberg.

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a>Entrada

### <a name="bitsprecision--int"></a>bitsPrecision: [int](xref:microsoft.quantum.lang-ref.int)

Isso fornece uma estimativa de $ \phi $ com o desvio padrão $ \sigma \le 2 \ pi/2 ^ \text{bitsPrecision} $ usando várias consultas dimensionando como $ \sigma \le 10,7 \pi/\Text{# de consultas} $.


### <a name="oracle--discreteoracle"></a>Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Uma operação que implementa $U ^ m $ para potências de inteiros fornecidas $m $.


### <a name="targetstate--qubit"></a>TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Uma Quantum registra que $U $ age. Se ele armazenar um eigenstate $ \ket{\phi} $ de $U $, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ para $ \phi\in (-\pi, \pi] $ uma fase desconhecida.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Comentários

No limite de um grande número de consultas, Cramer-Rao limites inferiores para o desvio padrão da estimativa de $ \phi $ satisfazem $ \sigma \ge 2 \pi/\Text{# de consultas} $.

## <a name="references"></a>Referências

- Calibragem robusta de um Single-Qubit universal Gate-Set por meio da estimativa de fase robusta Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677