---
title: 'Q # introdution'
description: 'Introdução rápida aos programas Quantum em p #'
author: beheim
ms.author: beheim
ms.date: 11/08/2020
ms.topic: article
uid: microsoft.quantum.guide.programs
ms.openlocfilehash: 975bcda5e0042406b465a83f17f1d2d3f5a1ec4f
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96233113"
---
# <a name="q-quantum-programming-language"></a><span data-ttu-id="fe1c8-103">Linguagem de programação da Quantum Q #</span><span class="sxs-lookup"><span data-stu-id="fe1c8-103">Q# Quantum Programming Language</span></span>

<span data-ttu-id="fe1c8-104">Tudo o que você precisa saber sobre a linguagem de programação Q # é detalhado no [Guia de linguagem do q #](xref:microsoft.quantum.qsharp.index).</span><span class="sxs-lookup"><span data-stu-id="fe1c8-104">Everything you need to know about the Q# programming language is detailed in the [Q# language guide](xref:microsoft.quantum.qsharp.index).</span></span> <span data-ttu-id="fe1c8-105">Como qualquer outra coisa, nosso [processo de design de linguagem](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) é software livre e as contribuições são bem-vindas.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-105">Like anything else, our [language design process](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) is open source and we welcome contributions.</span></span>
<span data-ttu-id="fe1c8-106">Para obter mais informações sobre as bases e a motivação por trás de Q #, consulte [por que precisamos de q #?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span><span class="sxs-lookup"><span data-stu-id="fe1c8-106">For more background about the foundations and motivation behind Q#, see [Why do we need Q#?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span></span>  
<span data-ttu-id="fe1c8-107">O Q # é fornecido como parte do kit de desenvolvimento Quantum (QDK) para uma visão geral rápida, confira [o que é o QDK?](xref:microsoft.quantum.overview.q-sharp).</span><span class="sxs-lookup"><span data-stu-id="fe1c8-107">Q# is shipped as part of the Quantum Development Kit (QDK) For a quick overview, check out [What is the QDK?](xref:microsoft.quantum.overview.q-sharp).</span></span> 

## <a name="what-is-a-quantum-program"></a><span data-ttu-id="fe1c8-108">O que é um programa Quantum?</span><span class="sxs-lookup"><span data-stu-id="fe1c8-108">What is a quantum program?</span></span>

<span data-ttu-id="fe1c8-109">Um programa Quantum pode ser visto como um conjunto específico de sub-rotinas clássicas que, quando chamado, executam uma computação interagindo com um sistema Quantum; um programa escrito em Q # não modele diretamente o estado Quantum, mas descreve como um computador de controle clássico interage com o qubits.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-109">A quantum program can be seen as a particular set of classical subroutines which, when called, perform a computation by interacting with a quantum system; a program written in Q# does not directly model the quantum state, but rather describes how a classical control computer interacts with qubits.</span></span>
<span data-ttu-id="fe1c8-110">Isso nos permite ser totalmente independente do que um estado Quantum ainda *está* em cada computador de destino, que pode ter interpretações diferentes dependendo do computador.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-110">This allows us to be entirely agnostic about what a quantum state even *is* on each target machine, which might have different interpretations depending on the machine.</span></span> 

<span data-ttu-id="fe1c8-111">Uma consequência importante disso é que Q # não tem a capacidade de introspecção no estado de um qubit ou outras propriedades da mecânica quantum diretamente, o que garante que um programa Q # possa ser fisicamente executado em um computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-111">An important consequence of that is that Q# has no ability to introspect into the state of a qubit or other properties of quantum mechanics directly, which guarantees that a Q# program can be physically executed on a quantum computer.</span></span>
<span data-ttu-id="fe1c8-112">Em vez disso, um programa pode chamar operações como [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) para extrair informações clássicas de um qubit.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-112">Instead, a program can call operations such as [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) to extract classical information from a qubit.</span></span>

<span data-ttu-id="fe1c8-113">Uma vez alocados, um qubit pode ser passado para operações e funções, também conhecido como *callables*.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-113">Once allocated, a qubit can be passed to operations and functions, also referred to as *callables*.</span></span> <span data-ttu-id="fe1c8-114">De certa forma, isso é tudo o que um programa Q # pode fazer com um qubit; Todas as ações diretas no estado de um qubit são definidas por chamadores *intrínsecos* , como [`X`](xref:Microsoft.Quantum.Intrinsic.X) and [`H`](xref:Microsoft.Quantum.Intrinsic.H) -ex. callables, cujas implementações não são definidas em Q #, mas, em vez disso, são definidas pelo computador de destino.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-114">In some sense, this is all that a Q# program can do with a qubit; Any direct actions on state of a qubit are all defined by *intrinsic* callables such as [`X`](xref:Microsoft.Quantum.Intrinsic.X) and [`H`](xref:Microsoft.Quantum.Intrinsic.H) - i.e. callables whose implementations are not defined within Q# but are instead defined by the target machine.</span></span> <span data-ttu-id="fe1c8-115">O que essas operações realmente *fazem* é apenas concreto pelo computador de destino que usamos para executar o programa Q # específico.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-115">What these operations actually *do* is only made concrete by the target machine we use to run the particular Q# program.</span></span>

<span data-ttu-id="fe1c8-116">Por exemplo, se estiver executando o programa em nosso [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), o simulador executará as operações matemáticas correspondentes para o sistema Quantum simulado.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-116">For example, if running the program on our [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), the simulator performs the corresponding mathematical operations to the simulated quantum system.</span></span>
<span data-ttu-id="fe1c8-117">Mas olhando para o futuro, quando o computador de destino for um computador Quantum real, chamar tais operações em Q # direcionará o computador Quantum para executar as operações *reais* correspondentes no sistema Quantum *real* (por exemplo, os pulsos de laser com precisão de tempo).</span><span class="sxs-lookup"><span data-stu-id="fe1c8-117">But looking toward the future, when the target machine is a real quantum computer, calling such operations in Q# will direct the quantum computer to perform the corresponding *real* operations on the *real* quantum system (e.g. precisely timed laser pulses).</span></span>

<span data-ttu-id="fe1c8-118">Um programa Q # recombina essas operações conforme definido por um computador de destino para criar operações novas e de nível mais alto para a computação da Quantum Express.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-118">A Q# program recombines these operations as defined by a target machine to create new, higher-level operations to express quantum computation.</span></span>
<span data-ttu-id="fe1c8-119">Dessa forma, Q # torna fácil expressar os algoritmos Quantum subjacente e Quantum híbrido-clássico, além de ser geral em relação à estrutura de um computador de destino ou simulador.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-119">In this way, Q# makes it easy to express the logic underlying quantum and hybrid quantum–classical algorithms, while also being general with respect to the structure of a target machine or simulator.</span></span>

<span data-ttu-id="fe1c8-120">Um exemplo simples é o seguinte programa, que aloca um qubit no estado $ \ket {0} $, depois aplica uma operação Hadamard `H` a ele e mede o resultado na `PauliZ` base.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-120">A simple example is the following program, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
@EntryPoint()
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

<span data-ttu-id="fe1c8-121">Nosso [katas Quantum](https://github.com/microsoft/QuantumKatas#introduction) fornece uma boa introdução sobre [conceitos de computação Quantum](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) , como operações de Quantum comuns e como manipular o qubits.</span><span class="sxs-lookup"><span data-stu-id="fe1c8-121">Our [Quantum Katas](https://github.com/microsoft/QuantumKatas#introduction) give a good introduction on [Quantum Computing Concepts](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) such as common quantum operations and how to manipulate qubits.</span></span> <span data-ttu-id="fe1c8-122">Mais exemplos também podem ser encontrados em [operações intrínsecas e funções](xref:microsoft.quantum.libraries.standard.prelude).</span><span class="sxs-lookup"><span data-stu-id="fe1c8-122">More examples can also be found in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude).</span></span>



