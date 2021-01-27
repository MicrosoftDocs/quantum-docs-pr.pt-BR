---
uid: Microsoft.Quantum.Simulation.EstimateEnergy
title: Operação EstimateEnergy
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergy
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: f9243557718e12d168afadbf641492291afd1704
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856758"
---
# <a name="estimateenergy-operation"></a>Operação EstimateEnergy

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa a preparação do estado aplicando um `statePrepUnitary` em uma estimativa de fase de estado de entrada alocada automaticamente em relação ao `qpeUnitary` estado resultante usando um `phaseEstAlgorithm` .

```qsharp
operation EstimateEnergy (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a>Entrada

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Número de qubits usadas para executar a simulação.


### <a name="stateprepunitary--qubit--unit"></a>statePrepUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Um Oracle representando a preparação do estado para o gerador dinâmico inicial.


### <a name="qpeunitary--qubit--unit--is-adj--ctl"></a>qpeUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

Um Oracle que representa um operador unitário $U $ representando a evolução do tempo $ \delta t $ em um gerador dinâmico com estado de terra $ \ket{\phi} $ e energia de estado terrestre $E = \phi \\ , \delta t $.


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a>phaseEstAlgorithm: ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [duplo](xref:microsoft.quantum.lang-ref.double) 

Uma operação que executa a estimativa de fase em uma determinada operação de unitário.
Consulte [estimativa de fase iterativa](/quantum/libraries/characterization#iterative-phase-estimation) para obter mais detalhes.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)

Uma estimativa de $ \hat{\phi} $ do estado do solo Energy $ \phi $ da energia de estado terrestre do gerador representado pelo $U $.