---
title: Teoria de Hartree-Fock
description: Saiba mais sobre a teoria do Hartree – Fock, uma maneira simples de construir o estado inicial para sistemas Quantum.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.hartreefock
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2d5e597c36f7873dfd1e011e7ce7d4b01c0f786e
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869537"
---
# <a name="hartreefock-theory"></a><span data-ttu-id="3bad3-103">Hartree – teoria de Fock</span><span class="sxs-lookup"><span data-stu-id="3bad3-103">Hartree–Fock Theory</span></span>

<span data-ttu-id="3bad3-104">Talvez a quantidade mais importante na simulação química do Quantum seja o estado do solo, que é o eigenvector de energia mínimo da matriz Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="3bad3-104">Perhaps the most important quantity in quantum chemistry simulation is the ground state, which is the minimum energy eigenvector of the Hamiltonian matrix.</span></span>
<span data-ttu-id="3bad3-105">Isso ocorre porque, para a maioria das moléculas, as quantidades de temperatura da sala, como as taxas de reação, são dominadas por diferenças de energia gratuitas entre os Estados da Quantum que descrevem o início e o final de uma etapa em um percurso de reação e, na temperatura da sala, tal estado intermediário geralmente são Estados básicos</span><span class="sxs-lookup"><span data-stu-id="3bad3-105">This is because for most molecules at room temperature quantities such as reaction rates are dominated by free energy differences between quantum states that describe the beginning and end of a step in a reaction pathway and at room temperature such intermediate state are usually ground states.</span></span>
<span data-ttu-id="3bad3-106">Embora o estado de terra normalmente seja muito difícil de aprender (mesmo com um computador Quantum) porque é uma distribuição em um número exponencialmente grande de configurações.</span><span class="sxs-lookup"><span data-stu-id="3bad3-106">While the ground state is typically too hard to learn (even with a quantum computer) because it is a distribution over an exponentially large number of configurations.</span></span>
<span data-ttu-id="3bad3-107">Quantidades como energia de estado terrestre podem ser aprendidas.</span><span class="sxs-lookup"><span data-stu-id="3bad3-107">Quantities such as ground state energy can be learned.</span></span>
<span data-ttu-id="3bad3-108">Por exemplo, se $ \ket{\psi} $ for qualquer estado de Quantum puro, então \begin{Equation} E = \bra{\psi} \hat{H} \ket{\psi} \end{Equation} proporcionará a energia média que o sistema tem nesse estado.</span><span class="sxs-lookup"><span data-stu-id="3bad3-108">For example, if $\ket{\psi}$ is any pure quantum state then \begin{equation} E = \bra{ \psi } \hat{H} \ket{\psi} \end{equation} gives the mean energy that the system has in that state.</span></span>
<span data-ttu-id="3bad3-109">O estado de aterramento é o estado que fornece o menor valor desse.</span><span class="sxs-lookup"><span data-stu-id="3bad3-109">The ground state then is the state that gives the smallest such value.</span></span> <span data-ttu-id="3bad3-110">Como resultado, escolher um estado que seja o mais próximo possível do estado de terra real é vitalmente importante para estimar a energia diretamente (como é feito no eigensolvers de variação) ou por meio de estimativa de fase.</span><span class="sxs-lookup"><span data-stu-id="3bad3-110">As a result, choosing a state that is as close as possible to the true ground state is vitally important for estimating the energy either directly (as is done in variational eigensolvers) or through phase estimation.</span></span>

<span data-ttu-id="3bad3-111">Hartree – a teoria de Fock oferece uma maneira simples de construir o estado inicial para sistemas Quantum.</span><span class="sxs-lookup"><span data-stu-id="3bad3-111">Hartree–Fock theory gives a simple way to construct the initial state for quantum systems.</span></span> <span data-ttu-id="3bad3-112">Ele produz uma única aproximação Slater-determinante para o estado de aterramento de um sistema Quantum.</span><span class="sxs-lookup"><span data-stu-id="3bad3-112">It yields a single Slater-determinant approximation to the ground state of a quantum system.</span></span> <span data-ttu-id="3bad3-113">Para esse fim, ele encontra uma rotação no Fock que minimiza a energia do estado do solo.</span><span class="sxs-lookup"><span data-stu-id="3bad3-113">To that end, it finds a rotation within Fock-space that minimizes the ground state energy.</span></span> <span data-ttu-id="3bad3-114">Em particular, para um sistema de $N $ elétrons, o método executa a rotação \begin{Equation} \ prod_ {j = 0} ^ {N-1} a ^ \ dagger_j \ket {0} \mapsto \ prod_ {j = 0} ^ {N-1} e ^ {u} a ^ \ dagger_j e ^ {-u} \ket {0} \defeq\ prod_ {j = 0} ^ {N-1} \widetilde{a} ^ \ dagger_j \ket {0} , \End{Equation} com um Hermitian (ou seja, $u =-u ^ \dagger $) Matrix $u = \ sum_ {pq} U_ {pq} a ^ \ dagger_p a_q $.</span><span class="sxs-lookup"><span data-stu-id="3bad3-114">In particular, for a system of $N$ electrons the method performs the rotation \begin{equation} \prod_{j=0}^{N-1} a^\dagger_j \ket{0} \mapsto \prod_{j=0}^{N-1} e^{u} a^\dagger_j e^{-u} \ket{0}\defeq\prod_{j=0}^{N-1}  \widetilde{a}^\dagger_j  \ket{0}, \end{equation} with an anti-Hermitian (i.e. $u= -u^\dagger$) matrix $u = \sum_{pq} u_{pq} a^\dagger_p a_q$.</span></span> <span data-ttu-id="3bad3-115">Deve-se observar que a matriz $u $ representa as rotações orbital e $ \widetilde{a} ^ \ dagger_j $ e $ \widetilde{a} _j $ representam os operadores de criação e Annihilation para elétrons ocupando Hartree – Fock molecular spin-órbitas.</span><span class="sxs-lookup"><span data-stu-id="3bad3-115">It should be noted that the matrix $u$ represents the orbital rotations and $\widetilde{a}^\dagger_j$ and $\widetilde{a}_j$ represent creation and annihilation operators for electrons occupying Hartree–Fock molecular spin-orbitals.</span></span>


<span data-ttu-id="3bad3-116">A matriz $u $ é então otimizada para minimizar a energia esperada $ \bra {0} \ prod_ {j = 0} ^ {n-1} \widetilde{a} \_ j H \prod \_ {k = 0} ^ {n-1} \widetilde{a} ^ \ dagger_k \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="3bad3-116">The matrix $u$ is then optimized to minimize the expected energy $\bra{0} \prod_{j=0}^{N-1}  \widetilde{a}\_j  H \prod\_{k=0}^{N-1}  \widetilde{a}^\dagger_k\ket{0}$.</span></span> <span data-ttu-id="3bad3-117">Embora esses problemas de otimização possam ser genericamente difíceis, na prática, o algoritmo Hartree – Fock tende a convergir rapidamente para uma solução quase ideal para o problema de otimização, especialmente para moléculas de shell fechado nas geometrias de equilíbrio.</span><span class="sxs-lookup"><span data-stu-id="3bad3-117">While such optimization problems may be generically hard, in practice the Hartree–Fock algorithm tends to rapidly converge to a near-optimal solution to the optimization problem, especially for closed-shell molecules in the equilibrium geometries.</span></span> <span data-ttu-id="3bad3-118">Podemos especificar esses Estados como uma instância do `FermionWavefunction` objeto.</span><span class="sxs-lookup"><span data-stu-id="3bad3-118">We may specify these states as an instance of the `FermionWavefunction` object.</span></span> <span data-ttu-id="3bad3-119">Por exemplo, o estado $a ^ \ dagger_ {1} um ^ \ dagger_ {2} um ^ \ dagger_ {6} \ket {0} $ é instanciado na biblioteca química da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="3bad3-119">For instance, the state $a^\dagger_{1}a^\dagger_{2}a^\dagger_{6}\ket{0}$ is instantiated in the chemistry library as follows.</span></span>
```csharp
// Create a list of integer indices of the creation operators
var indices = new[] { 1, 2, 6 };

// Convert the list of indices to a `FermionWavefunction` object.
// In this case, the indices are integers, so we use the `int`
// type specialization.
var wavefunction = new FermionWavefunction<int>(indices);
```
<span data-ttu-id="3bad3-120">Também é possível indexar funções de onda com `SpinOrbital` índices e, em seguida, converter esses índices em inteiros da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="3bad3-120">It is also possible to index wave functions with `SpinOrbital` indices, and then convert these indices to integers as follows.</span></span>
```csharp
// Create a list of spin orbital indices of the creation operators
var indices = new[] { (0, Spin.d), (1,Spin.u), (3, Spin.u) };

// Convert the list of indices to a `FermionWavefunction` object.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(indices.ToSpinOrbitals());

// Convert a wavefunction indexed by spin orbitals to
// one indexed by integers
var wavefunctionInt = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

<span data-ttu-id="3bad3-121">O recurso mais surpreendente sobre a teoria Hartree – Fock é que ele produz um estado Quantum que não tem nenhum Entanglement entre o elétrons.</span><span class="sxs-lookup"><span data-stu-id="3bad3-121">The most striking feature about Hartree–Fock theory is that it yields a quantum state that has no entanglement between the electrons.</span></span>
<span data-ttu-id="3bad3-122">Isso significa que ele geralmente fornece uma descrição qualitativa adequada das propriedades de sistemas molecular.</span><span class="sxs-lookup"><span data-stu-id="3bad3-122">This means that it often provides a suitable qualitative description of properties of molecular systems.</span></span> 

<span data-ttu-id="3bad3-123">O estado Hartree-Fock também pode ser reconstruído a partir de um da `FermionHamiltonian` seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="3bad3-123">The Hartree-Fock state may also be reconstructed from a `FermionHamiltonian`  as follows.</span></span>
```csharp
// We initialize a fermion Hamiltonian.
var fermionHamiltonian = new FermionHamiltonian();

// Create a Hartree-Fock state from the Hamiltonian 
// with, say, `4` occupied spin orbitals.
var wavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons: 4);
```

<span data-ttu-id="3bad3-124">No entanto, obter resultados precisos, especialmente para sistemas altamente correlacionados, precisa de Estados de Quantum que vão além da teoria Hartree – Fock.</span><span class="sxs-lookup"><span data-stu-id="3bad3-124">However, obtaining accurate results, especially for strongly correlated systems, necessitate quantum states that go beyond Hartree–Fock theory.</span></span>
