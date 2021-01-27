---
title: Carregar um Hamiltonian do arquivo
description: Saiba como gerar automaticamente um Hamiltonian grande usando o esquema Broombridge.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: sample
uid: microsoft.quantum.chemistry.examples.loadhamiltonian
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4bd663ade7649be05058f07bee1acf541ec3e487
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844112"
---
# <a name="loading-a-hamiltonian-from-file"></a>Carregar um Hamiltonian do arquivo
Anteriormente, construímos o Hamiltonians adicionando termos individuais a ele. Embora isso seja bom para exemplos pequenos, o quantum química em escala exige Hamiltonians com milhões ou bilhões de termos. Tais Hamiltonians, gerados por pacotes de química, como NWChem, são muito grandes para serem importados manualmente. Neste exemplo, ilustramos como uma `FermionHamiltonian` instância pode ser gerada automaticamente de um molécula representado pelo [esquema Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge). Para referência, é possível inspecionar o `LithiumHydrideGUI` exemplo fornecido ou o `RunSimulation` exemplo. O suporte limitado também está disponível para importação a partir do formato consumido por [LIQUi |>](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/).

Vamos considerar o exemplo do nitrogen molécula, que é fornecido na `IntegralData/YAML` pasta do repositório de exemplos. O método para carregar o `Broombridge` esquema é simples.

```csharp
// This is the name of the file we want to load
var filename = @"n2_1_00Re_sto3g.nw.out.yaml";
// This is the directory containing the file
var root = @"IntegralData\YAML";

// This deserializes a Broombridge file, given its filename.
var broombridge = Broombridge.Deserializers.DeserializeBroombridge($@"{root}\{filename}");

// Note that the deserializer returns a list of `ProblemDescription` instances 
// as the file might describe multiple Hamiltonians. In this example, there is 
// only one Hamiltonian. So we use `.First()`, which selects the first element of the list.
var problem = broombridge.ProblemDescriptions.First();

// This extracts the `OrbitalIntegralHamiltonian` from Broombridge format,
// then converts it to a fermion Hamiltonian, then to a Jordan-Wigner
// representation.
var orbitalIntegralHamiltonian = problem.OrbitalIntegralHamiltonian;
var fermionHamiltonian = orbitalIntegralHamiltonian.ToFermionHamiltonian(IndexConvention.UpDown);
var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);
```

O esquema Broombridge também contém sugestões para que o estado inicial seja preparado. Os rótulos, por exemplo `"|G⟩"` `"|E1⟩"` , ou, para esses Estados podem ser vistos inspecionando o arquivo. Para preparar esses Estados iniciais, o `qSharpData` consumido pelos Q# algoritmos Quantum é obtido de forma semelhante à [seção anterior](xref:microsoft.quantum.chemistry.examples.energyestimate), mas com um parâmetro adicional selecionando o estado inicial desejado. Por exemplo,
```csharp
// The desired initial state, assuming that a description of it is present in the
// Broombridge schema.
var state = "|E1>";
var wavefunction = problem.Wavefunctions[state].ToIndexing(IndexConvention.UpDown);

// This creates the qSharpData consumable by the Q# chemistry library algorithms.
var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
var qSharpWavefunctionData = wavefunction.ToQSharpFormat();
var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Todas as etapas acima podem ser abreviadas usando métodos de conveniência fornecidos a seguir.
```csharp
// This is the name of the file we want to load
var filename = "...";

// This deserializes a Broombridge file, given its filename.
var broombridge = Broombridge.Deserializers.DeserializeBroombridge(filename);

// Note that the deserializer returns a list of `ProblemDescription` instances 
// as the file might describe multiple Hamiltonians. In this example, there is 
// only one Hamiltonian. So we use `.Single()`, which selects the only element of the list.
var problem = broombridge.ProblemDescriptions.Single();

// This is a data structure representing the Jordan-Wigner encoding 
// of the Hamiltonian that we may pass to a Q# algorithm.
// If no state is specified, the Hartree-Fock state is used by default.
var qSharpData = problem.ToQSharpFormat("|E1>");
```

Também poderemos carregar um Hamiltonian do LIQUi |> formato, usando uma sintaxe muito semelhante. 

```csharp
// This is the name of the file we want to load
var filename = @"fe2s2_sto3g.dat"; // This is Ferrodoxin.
// This is the directory containing the file
var root = @"IntegralData\Liquid";

// Deserialize the LiQuiD format.
var problem = LiQuiD.Deserialize($@"{root}\{filename}").First();

// This is a data structure representing the Jordan-Wigner encoding 
// of the Hamiltonian that we may pass to a Q# algorithm.
var qSharpData = problem.ToQSharpFormat();
```

Seguindo esse processo de qualquer instância de Broombridge, ou qualquer etapa intermediária, os algoritmos Quantum, como a estimativa de fase Quantum, podem ser executados no problema de estrutura eletrônica especificado.
