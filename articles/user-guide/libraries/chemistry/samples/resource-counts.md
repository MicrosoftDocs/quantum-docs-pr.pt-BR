---
title: Obter contagens de recursos
description: Saiba como obter estimativas de recursos usando um simulador de rastreamento Quantum.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: sample
uid: microsoft.quantum.chemistry.examples.resourcecounts
no-loc:
- Q#
- $$v
ms.openlocfilehash: b8974114a5629fa1928b5774e79aba93fa3d1f7d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856234"
---
# <a name="obtaining-resource-counts"></a>Obter contagens de recursos

O custo da simulação de $n $ qubits em computadores clássicos é dimensionado exponencialmente com $n $. Isso limita bastante o tamanho de uma simulação de química do Quantum que pode ser executada com o simulador de estado completo. Para grandes instâncias de química, poderemos, no entanto, obter informações úteis. Aqui, examinamos como os custos de recursos, como o número de T-Gates ou CNOT Gates, para simular a química podem ser obtidos de maneira automatizada usando o [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Essas informações informam quando os computadores Quantum podem ser grandes o suficiente para executar esses algoritmos de química da Quantum. Para referência, consulte o `GetGateCount` exemplo fornecido.

Vamos supor que já temos uma `FermionHamiltonian` instância, digamos, carregada do esquema Broombridge, conforme discutido no exemplo de [carregamento de arquivo](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) . 

```csharp
    // Filename of Hamiltonian to be loaded.
    var filename = "...";

    // This deserializes Broombridge.
    var problem = Broombridge.Deserializers.DeserializeBroombridge(filename).ProblemDescriptions.First();

    // This is a data structure representing the Jordan-Wigner encoding 
    // of the Hamiltonian that we may pass to a Q# algorithm.
    var qSharpData = problem.ToQSharpFormat();
```

A sintaxe para obter estimativas de recursos é quase idêntica à execução do algoritmo no simulador de estado completo. Simplesmente escolhemos um computador de destino diferente. Para fins de estimativas de recursos, é suficiente avaliar o custo de uma única etapa Trotter ou uma movimentação Quantum criada pela técnica Qubitization. O texto clichê para invocar esses algoritmos é o seguinte.

```qsharp
//////////////////////////////////////////////////////////////////////////
// Using Trotterization //////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single Trotter step.
operation RunTrotterStep (qSharpData: JordanWignerEncodingData) : Unit {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    // We use a Product formula, also known as `Trotterization` to
    // simulate the Hamiltonian.
    // The integrator step size does not affect the gate cost of a single step.
    let trotterStepSize = 1.0;
    
    // Order of integrator
    let trotterOrder = 1;
    let (nQubits, (rescaleFactor, oracle)) = TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // We not allocate qubits an run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
}


//////////////////////////////////////////////////////////////////////////
// Using Qubitization ////////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single qubitization step.
operation RunQubitizationStep (qSharpData: JordanWignerEncodingData) : Double {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nQubits, (l1Norm, oracle)) = QubitizationOracle(qSharpData);
    
    // We now allocate qubits and run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
    
    return l1Norm;
}
```

Agora, configuramos o simulador de rastreamento para acompanhar os recursos nos quais estamos interessados. Nesse caso, contamos as operações Quantum primitivas definindo o `usePrimitiveOperationsCounter` sinalizador como `true` . Um detalhe técnico `throwOnUnconstraintMeasurement` é definido como `false` para evitar exceções em casos em que o Q# código não declara corretamente a probabilidade de resultados de medida, se algum for executado.

```csharp
private static QCTraceSimulator CreateAndConfigureTraceSim()
{
    // Create and configure Trace Simulator
    var config = new QCTraceSimulatorConfiguration()
    {
        usePrimitiveOperationsCounter = true,
        throwOnUnconstraintMeasurement = false
    };

    return new QCTraceSimulator(config);
}
```

Agora, executamos o algoritmo Quantum do programa de driver da seguinte maneira.

```csharp
// Instantiate a trace simulator instance
QCTraceSimulator sim = CreateAndConfigureTraceSim();

// Run the quantum algorithm on the trace simulator.
RunQubitizationStep.Run(sim, qSharpData);

// Print all resource counts to file.
var gateStats = sim.ToCSV();
foreach (var x in gateStats)
{
    System.IO.File.WriteAllLines($"QubitizationGateCountEstimates.{x.Key}.csv", new string[] { x.Value });
}
```