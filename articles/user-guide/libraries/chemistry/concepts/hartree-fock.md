---
title: Teoria de Hartree-Fock
description: Saiba mais sobre a teoria do Hartree – Fock, uma maneira simples de construir o estado inicial para sistemas Quantum.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.hartreefock
ms.openlocfilehash: 6fa63cbe13fe98565ffb42b56f3ade86720cedb3
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274311"
---
# <a name="hartreefock-theory"></a>Hartree – teoria de Fock

Talvez a quantidade mais importante na simulação química do Quantum seja o estado do solo, que é o eigenvector de energia mínimo da matriz Hamiltonian.
Isso ocorre porque, para a maioria das moléculas, as quantidades de temperatura da sala, como as taxas de reação, são dominadas por diferenças de energia gratuitas entre os Estados da Quantum que descrevem o início e o final de uma etapa em um percurso de reação e, na temperatura da sala, tal estado intermediário geralmente são Estados básicos
Embora o estado de terra normalmente seja muito difícil de aprender (mesmo com um computador Quantum) porque é uma distribuição em um número exponencialmente grande de configurações.
Quantidades como energia de estado terrestre podem ser aprendidas.
Por exemplo, se $ \ket{\psi} $ for qualquer estado de Quantum puro, então \begin{Equation} E = \bra{\psi} \hat{H} \ket{\psi} \end{Equation} proporcionará a energia média que o sistema tem nesse estado.
O estado de aterramento é o estado que fornece o menor valor desse. Como resultado, escolher um estado que seja o mais próximo possível do estado de terra real é vitalmente importante para estimar a energia diretamente (como é feito no eigensolvers de variação) ou por meio de estimativa de fase.

Hartree – a teoria de Fock oferece uma maneira simples de construir o estado inicial para sistemas Quantum. Ele produz uma única aproximação Slater-determinante para o estado de aterramento de um sistema Quantum. Para esse fim, ele encontra uma rotação no Fock que minimiza a energia do estado do solo. Em particular, para um sistema de $N $ elétrons, o método executa a rotação \begin{Equation} \ prod_ {j = 0} ^ {N-1} a ^ \ dagger_j \ket {0} \mapsto \ prod_ {j = 0} ^ {N-1} e ^ {u} a ^ \ dagger_j e ^ {-u} \ket {0} \defeq\ prod_ {j = 0} ^ {N-1} \widetilde{a} ^ \ dagger_j \ket {0} , \End{Equation} com um Hermitian (ou seja, $u =-u ^ \dagger $) Matrix $u = \ sum_ {pq} U_ {pq} a ^ \ dagger_p a_q $. Deve-se observar que a matriz $u $ representa as rotações orbital e $ \widetilde{a} ^ \ dagger_j $ e $ \widetilde{a} _j $ representam os operadores de criação e Annihilation para elétrons ocupando Hartree – Fock molecular spin-órbitas.


A matriz $u $ é então otimizada para minimizar a energia esperada $ \bra {0} \ prod_ {j = 0} ^ {n-1} \widetilde{a} \_ j H \prod \_ {k = 0} ^ {n-1} \widetilde{a} ^ \ dagger_k \ket {0} $. Embora esses problemas de otimização possam ser genericamente difíceis, na prática, o algoritmo Hartree – Fock tende a convergir rapidamente para uma solução quase ideal para o problema de otimização, especialmente para moléculas de shell fechado nas geometrias de equilíbrio. Podemos especificar esses Estados como uma instância do `FermionWavefunction` objeto. Por exemplo, o estado $a ^ \ dagger_ {1} um ^ \ dagger_ {2} um ^ \ dagger_ {6} \ket {0} $ é instanciado na biblioteca química da seguinte maneira.
```csharp
// Create a list of integer indices of the creation operators
var indices = new[] { 1, 2, 6 };

// Convert the list of indices to a `FermionWavefunction` object.
// In this case, the indices are integers, so we use the `int`
// type specialization.
var wavefunction = new FermionWavefunction<int>(indices);
```
Também é possível indexar funções de onda com `SpinOrbital` índices e, em seguida, converter esses índices em inteiros da seguinte maneira.
```csharp
// Create a list of spin orbital indices of the creation operators
var indices = new[] { (0, Spin.d), (1,Spin.u), (3, Spin.u) };

// Convert the list of indices to a `FermionWavefunction` object.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(indices.ToSpinOrbitals());

// Convert a wavefunction indexed by spin orbitals to
// one indexed by integers
var wavefunctionInt = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

O recurso mais surpreendente sobre a teoria Hartree – Fock é que ele produz um estado Quantum que não tem nenhum Entanglement entre o elétrons.
Isso significa que ele geralmente fornece uma descrição qualitativa adequada das propriedades de sistemas molecular. 

O estado Hartree-Fock também pode ser reconstruído a partir de um da `FermionHamiltonian` seguinte maneira.
```csharp
// We initialize a fermion Hamiltonian.
var fermionHamiltonian = new FermionHamiltonian();

// Create a Hartree-Fock state from the Hamiltonian 
// with, say, `4` occupied spin orbitals.
var wavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons: 4);
```

No entanto, obter resultados precisos, especialmente para sistemas altamente correlacionados, precisa de Estados de Quantum que vão além da teoria Hartree – Fock.
