---
title: Obter estimativas do nível de energia
description: Percorra um programa de exemplo Q# que estima os valores de nível de energia de molecular Hydrogen.
author: guanghaolow
ms.author: gulow
ms.date: 07/02/2020
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
no-loc:
- Q#
- $$v
ms.openlocfilehash: 81fba0c52c854d61f9143659795fb4d3c3cee8b9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691528"
---
# <a name="obtaining-energy-level-estimates"></a>Obter estimativas do nível de energia
Estimar os valores dos níveis de energia é um dos principais aplicativos da quantum química. Este artigo descreve como você pode executar isso para o exemplo canônico de molecular Hydrogen. O exemplo referenciado nesta seção está [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/MolecularHydrogen) no repositório de exemplos de química. Um exemplo mais visual que plota a saída é a [`MolecularHydrogenGUI`](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/MolecularHydrogenGUI) demonstração.

## <a name="estimating-the-energy-values-of-molecular-hydrogen"></a>Estimando os valores de energia de molecular Hydrogen

A primeira etapa é construir o Hamiltonian que representa o molecular Hydrogen. Embora você possa construir isso usando a ferramenta NWChem, para resumir, este exemplo adiciona os termos de Hamiltonian manualmente.

```csharp
    // These orbital integrals are represented using the OrbitalIntegral
    // data structure.
    var energyOffset = 0.713776188; // This is the coulomb repulsion
    var nElectrons = 2; // Molecular hydrogen has two electrons
    var orbitalIntegrals = new OrbitalIntegral[]
    {
        new OrbitalIntegral(new[] { 0,0 }, -1.252477495),
        new OrbitalIntegral(new[] { 1,1 }, -0.475934275),
        new OrbitalIntegral(new[] { 0,0,0,0 }, 0.674493166),
        new OrbitalIntegral(new[] { 0,1,0,1 }, 0.181287518),
        new OrbitalIntegral(new[] { 0,1,1,0 }, 0.663472101),
        new OrbitalIntegral(new[] { 1,1,1,1 }, 0.697398010),
        // This line adds the identity term.
        new OrbitalIntegral(new int[] { }, energyOffset)
    };

    // Initialize a fermion Hamiltonian data structure and add terms to it.
    var fermionHamiltonian = new OrbitalIntegralHamiltonian(orbitalIntegrals).ToFermionHamiltonian();
```

A simulação do Hamiltonian requer a conversão dos operadores Fermion em operadores qubit. Essa conversão é executada por meio da codificação Jordan-Wigner da seguinte maneira:

```csharp
    // The Jordan-Wigner encoding converts the fermion Hamiltonian, 
    // expressed in terms of fermionic operators, to a qubit Hamiltonian,
    // expressed in terms of Pauli matrices. This is an essential step
    // for simulating our constructed Hamiltonians on a qubit quantum
    // computer.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);

    // You also need to create an input quantum state to this Hamiltonian.
    // Use the Hartree-Fock state.
    var fermionWavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons);

    // This Jordan-Wigner data structure also contains a representation 
    // of the Hamiltonian and wavefunction made for consumption by the Q# operations.
    var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
    var qSharpWavefunctionData = fermionWavefunction.ToQSharpFormat();
    var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Em seguida, passe `qSharpData` , que representa o Hamiltonian, para a `TrotterStepOracle` função. `TrotterStepOracle` Retorna uma operação Quantum que aproxima a evolução em tempo real do Hamiltonian. Para obter mais informações, consulte [simulando o Hamiltonian Dynamics](xref:microsoft.quantum.chemistry.concepts.simulationalgorithms).

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);
```

Neste ponto, você pode usar os [algoritmos de estimativa de fase](xref:microsoft.quantum.libraries.characterization) da biblioteca padrão para aprender a energia de estado terrestre usando a simulação anterior. Isso requer a preparação de uma boa aproximação para o estado de aterramento do Quantum. As sugestões para essas aproximaçãos são fornecidas no [`Broombridge`](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) esquema. No entanto, essas sugestões estão ausentes, a abordagem padrão adiciona um número de `hamiltonian.NElectrons` elétrons para greedily minimizar o termo diagonal um-de energias. As funções e operações de estimativa de fase são fornecidas na notação de DocFX no namespace [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization) .

O trecho a seguir mostra como a saída de evolução em tempo real da biblioteca de simulação de química integra-se à estimativa de fase Quantum.

```qsharp
operation GetEnergyByTrotterization (
    qSharpData : JordanWignerEncodingData, 
    nBitsPrecision : Int, 
    trotterStepSize : Double, 
    trotterOrder : Int) : (Double, Double) {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nSpinOrbitals, fermionTermData, statePrepData, energyOffset) = qSharpData!;
    
    // Using a Product formula, also known as `Trotterization`, to
    // simulate the Hamiltonian.
    let (nQubits, (rescaleFactor, oracle)) = 
        TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // The operation that creates the trial state is defined here.
    // By default, greedy filling of spin-orbitals is used.
    let statePrep = PrepareTrialState(statePrepData, _);
    
    // Using the Robust Phase Estimation algorithm
    // of Kimmel, Low and Yoder.
    let phaseEstAlgorithm = RobustPhaseEstimation(nBitsPrecision, _, _);
    
    // This runs the quantum algorithm and returns a phase estimate.
    let estPhase = EstimateEnergy(nQubits, statePrep, oracle, phaseEstAlgorithm);
    
    // Now, obtain the energy estimate by rescaling the phase estimate
    // with the trotterStepSize. We also add the constant energy offset
    // to the estimated energy.
    let estEnergy = estPhase * rescaleFactor + energyOffset;
    
    // Return both the estimated phase and the estimated energy.
    return (estPhase, estEnergy);
}
```

Agora você pode invocar o Q# código do programa host. O código C# a seguir cria um simulador de estado completo e é executado `GetEnergyByTrotterization` para obter a energia de estado terrestre.

```csharp
using (var qsim = new QuantumSimulator())
{
    // Specify the bits of precision desired in the phase estimation 
    // algorithm
    var bits = 7;

    // Specify the step size of the simulated time evolution. The step size needs to
    // be small enough to avoid aliasing of phases, and also to control the
    // error of simulation.
    var trotterStep = 0.4;

    // Choose the Trotter integrator order
    Int64 trotterOrder = 1;

    // As the quantum algorithm is probabilistic, run a few trials.

    // This may be compared to true value of
    Console.WriteLine("Exact molecular hydrogen ground state energy: -1.137260278.\n");
    Console.WriteLine("----- Performing quantum energy estimation by Trotter simulation algorithm");
    for (int i = 0; i < 5; i++)
    {
        // EstimateEnergyByTrotterization
        var (phaseEst, energyEst) = GetEnergyByTrotterization.Run(qsim, qSharpData, bits, trotterStep, trotterOrder).Result;
    }
}
```

A operação retorna dois parâmetros: 

- `energyEst` é a estimativa da energia do estado de terra e deve estar próxima de `-1.137` em média. 
- `phaseEst` é a fase bruta retornada pelo algoritmo de estimativa de fase. Isso é útil para diagnosticar alias quando ocorre devido a um `trotterStep` valor muito grande.
