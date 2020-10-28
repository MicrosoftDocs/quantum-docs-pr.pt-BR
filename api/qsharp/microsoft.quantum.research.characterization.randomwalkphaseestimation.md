---
uid: Microsoft.Quantum.Research.Characterization.RandomWalkPhaseEstimation
title: Operação RandomWalkPhaseEstimation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Characterization
qsharp.name: RandomWalkPhaseEstimation
qsharp.summary: Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.
ms.openlocfilehash: 5e0c0871b916ff51b85dec8703111788b5204bc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693252"
---
# <a name="randomwalkphaseestimation-operation"></a>Operação RandomWalkPhaseEstimation

Namespace: [Microsoft. Quantum. Research. caracterization](xref:Microsoft.Quantum.Research.Characterization)

Agrupa [](https://nuget.org/packages/)


Executa estimativa de fase iterativa usando uma passagem aleatória para a inferência de Bayesiana aproximada nos resultados da medição clássica de um determinado Oracle e eigenstate.

```qsharp
operation RandomWalkPhaseEstimation (initialMean : Double, initialStdDev : Double, nMeasurements : Int, maxMeasurements : Int, unwind : Int, oracle : Microsoft.Quantum.Oracles.ContinuousOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a>Entrada

### <a name="initialmean--double"></a>initialMean: [Double](xref:microsoft.quantum.lang-ref.double)

Média da distribuição anterior inicial normal em relação a $ \phi $.


### <a name="initialstddev--double"></a>initialStdDev: [Double](xref:microsoft.quantum.lang-ref.double)

Desvio padrão da distribuição anterior inicial normal em relação a $ \phi $.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Número de medições a serem aceitas na estimativa final de posteriores.


### <a name="maxmeasurements--int"></a>maxMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Número total de medições que podem ser realizadas antes que a operação seja considerada como falha.


### <a name="unwind--int"></a>desenrolar: [int](xref:microsoft.quantum.lang-ref.int)

Número de resultados a serem esquecidos quando as verificações de consistência falham.


### <a name="oracle--continuousoracle"></a>Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)

Uma operação que representa um unitário $U $ de $U (t) \ket{\phi} = e ^ {i t \phi}\ket{\phi} $ for eigenstates $ \ket{\phi} $ com fase desconhecida $ \phi na \mathbb{R} ^ + $.


### <a name="targetstate--qubit"></a>TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro que $U $ age.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)

A estimativa final $ \hat{\phi} \mathrel{: =} \expect [\phi] $, em que a expectativa é sobre o posteriores dado todos os dados aceitos.

## <a name="remarks"></a>Comentários

### <a name="iterative-phase-estimation-and-eigenstates"></a>Estimativa e Eigenstates de fase iterativa

Em geral, o registro de entrada `eigenstate` não precisa ser um eigenstate $ \ket{\phi} $ de $U $, mas pode ser uma superposição em relação a eigenstates. Suponha que o estado de entrada seja fornecido por \begin{align} \ket{\psi} & = \sum \_ {j} \alpha \_ j \ket{\phi \_ j}, \end{Align}, em que $ \{ \alpha \_ j \} $ são coeficientes complexos, de modo que $ \sum \_ j | \alpha \_ j | ^ 2 = $1 e onde $U \ket{\phi \_ j} = \phi \_ j\ket {\ Phi \_ j} $.

Em seguida, executar estimativa de fase iterativa eventualmente convergirá para um único eigenstate, conforme descrito no [Guia de desenvolvimento](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates).

### <a name="experiment-design"></a>Design do experimento

Os tempos de medição $t $ e os ângulos de inversão $ \theta $ passados para `oracle` são escolhidos de acordo com a *heurística de adivinhação de partícula* , \Begin{align} \theta \sim \Pr (\phi), \quad t \approx \frac {1} {\variance{\phi}}.
\end{align} esse heurístico é ideal para reduzir a variância esperada de posteriores na estimativa de fase iterativa sob a hipótese de um normal anterior.

### <a name="optimality"></a>Ideais

Esta operação aproxima o estimador ideal para a fase $ \phi $, conforme avaliado usando a perda quadrática $L (\phi, \hat{\phi}) \mathrel{: =} (\phi-\hat{\phi}) ^ 2 $.

Consulte [estimativa de fase de Bayesiana](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) para obter mais detalhes sobre as estatísticas de estimativa de fase iterativa.

## <a name="references"></a>Referências

- Referencial *et al.* 2011 [doi: 10/TFX](https://doi.org/10.1007/s11128-012-0407-6), [arXiv: 1110.3067](https://arxiv.org/abs/1110.3067).
- Wiebe *et al.* 2013 [doi: 10/TF3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv: 1309.0876](https://arxiv.org/abs/1309.0876)
- Wiebe e granade 2018 *(na preparação)* .