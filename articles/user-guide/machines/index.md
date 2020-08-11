---
title: Simuladores quânticos e programas Q#
description: Descreve os simuladores quânticos disponíveis como computadores de destino para programas Q#.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 6/17/2020
ms.topic: article
uid: microsoft.quantum.machines
no-loc:
- Q#
- $$v
ms.openlocfilehash: 77401ca3642b89d708f338f852dc60bf7346b87b
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868297"
---
# <a name="quantum-simulators"></a><span data-ttu-id="5a35c-103">Simuladores quânticos</span><span class="sxs-lookup"><span data-stu-id="5a35c-103">Quantum simulators</span></span>

<span data-ttu-id="5a35c-104">Simuladores quânticos são programas de software executados em computadores clássicos e atuam como um *computador de destino* para um programa Q#. Assim, é possível executar e testar programas quânticos em um ambiente que prevê como os qubits reagem a diferentes operações.</span><span class="sxs-lookup"><span data-stu-id="5a35c-104">Quantum simulators are software programs that run on classical computers and act as the *target machine* for a Q# program, making it possible to run and test quantum programs in an environment that predicts how qubits will react to different operations.</span></span> <span data-ttu-id="5a35c-105">Este artigo descreve os simuladores quânticos incluídos no QDK (Quantum Development Kit) e maneiras diferentes de passar um programa Q# para os simuladores quânticos, por exemplo, por meio da linha de comando ou usando o código de driver escrito em uma linguagem clássica.</span><span class="sxs-lookup"><span data-stu-id="5a35c-105">This article describes which quantum simulators are included with the Quantum Development Kit (QDK), and different ways that you can pass a Q# program to the quantum simulators, for example, via the command line or by using driver code written in a classical language.</span></span>  



## <a name="the-quantum-development-kit-qdk-quantum-simulators"></a><span data-ttu-id="5a35c-106">Atualizar os simuladores quânticos do QDK (Quantum Development Kit)</span><span class="sxs-lookup"><span data-stu-id="5a35c-106">The Quantum Development Kit (QDK) quantum simulators</span></span>

<span data-ttu-id="5a35c-107">O simulador quântico é responsável por fornecer implementações de primitivos quânticos para o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="5a35c-107">The quantum simulator is responsible for providing implementations of quantum primitives for an algorithm.</span></span> <span data-ttu-id="5a35c-108">Isso inclui operações primitivas, como `H`, `CNOT` e `Measure`, bem como gerenciamento e acompanhamento de qubits.</span><span class="sxs-lookup"><span data-stu-id="5a35c-108">This includes primitive operations such as `H`, `CNOT`, and `Measure`, as well as qubit management and tracking.</span></span> <span data-ttu-id="5a35c-109">O QDK inclui diferentes classes de simuladores quânticos que representam modelos de execução diferentes para o mesmo algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="5a35c-109">The QDK includes different classes of quantum simulators representing different execution models for the same quantum algorithm.</span></span> 


<span data-ttu-id="5a35c-110">Cada tipo de simulador quântico pode fornecer diferentes implementações desses primitivos.</span><span class="sxs-lookup"><span data-stu-id="5a35c-110">Each type of quantum simulator can provide different implementations of these primitives.</span></span> <span data-ttu-id="5a35c-111">Por exemplo, o [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator) executa o algoritmo quântico ao simular totalmente o [vetor de estado quântico](xref:microsoft.quantum.glossary#quantum-state), enquanto o [simulador de rastreamento de computador quântico](xref:microsoft.quantum.machines.qc-trace-simulator.intro) não considera o estado quântico real.</span><span class="sxs-lookup"><span data-stu-id="5a35c-111">For example, the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator) runs the quantum algorithm by fully simulating the [quantum state vector](xref:microsoft.quantum.glossary#quantum-state), whereas the [quantum computer trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) doesn't consider the actual quantum state at all.</span></span> <span data-ttu-id="5a35c-112">Em vez disso, ele rastreia o uso de portões, qubits e outros recursos para o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="5a35c-112">Rather, it tracks gate, qubit, and other resource usage for the algorithm.</span></span>

### <a name="quantum-machine-classes"></a><span data-ttu-id="5a35c-113">Classes de computador quântico</span><span class="sxs-lookup"><span data-stu-id="5a35c-113">Quantum machine classes</span></span>

<span data-ttu-id="5a35c-114">No futuro, o QDK definirá classes adicionais de computadores quânticos para dar suporte a outros tipos de simulação e a execução em hardware quântico.</span><span class="sxs-lookup"><span data-stu-id="5a35c-114">In the future, the QDK will define additional quantum machine classes to support other types of simulation and to support execution on quantum hardware.</span></span> <span data-ttu-id="5a35c-115">Permitir que o algoritmo permaneça constante enquanto varia a implementação de computador subjacente facilita o teste e a depuração de um algoritmo em simulação e, em seguida, executa-o em um hardware real com a confiança de que o algoritmo não foi alterado.</span><span class="sxs-lookup"><span data-stu-id="5a35c-115">Allowing the algorithm to stay constant while varying the underlying machine implementation makes it easy to test and debug an algorithm in simulation and then run it on real hardware with confidence that the algorithm hasn't changed.</span></span>

<span data-ttu-id="5a35c-116">O QDK inclui várias classes de computadores quânticos, todas definidas no namespace `Microsoft.Quantum.Simulation.Simulators`.</span><span class="sxs-lookup"><span data-stu-id="5a35c-116">The QDK includes several quantum machine classes, all defined in the `Microsoft.Quantum.Simulation.Simulators` namespace.</span></span>

|<span data-ttu-id="5a35c-117">Simulador</span><span class="sxs-lookup"><span data-stu-id="5a35c-117">Simulator</span></span> |<span data-ttu-id="5a35c-118">Classe</span><span class="sxs-lookup"><span data-stu-id="5a35c-118">Class</span></span>|<span data-ttu-id="5a35c-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a35c-119">Description</span></span>|
|-----|------|---|
|[<span data-ttu-id="5a35c-120">Simulador de estado completo</span><span class="sxs-lookup"><span data-stu-id="5a35c-120">Full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator)| `QuantumSimulator` | <span data-ttu-id="5a35c-121">Executa e depura algoritmos quânticos e é limitado a cerca de 30 qubits.</span><span class="sxs-lookup"><span data-stu-id="5a35c-121">Runs and debugs quantum algorithms, and is limited to about 30 qubits.</span></span> |
|[<span data-ttu-id="5a35c-122">Avaliador de recursos simples</span><span class="sxs-lookup"><span data-stu-id="5a35c-122">Simple resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)| `ResourcesEstimator` | <span data-ttu-id="5a35c-123">Realiza uma análise de nível superior dos recursos necessários para executar um algoritmo quântico e dá suporte a milhares de qubits.</span><span class="sxs-lookup"><span data-stu-id="5a35c-123">Performs a top level analysis of the resources needed to run a quantum algorithm, and supports thousands of qubits.</span></span>|
|[<span data-ttu-id="5a35c-124">Avaliador de recursos baseado em rastreamento</span><span class="sxs-lookup"><span data-stu-id="5a35c-124">Trace-based resource estimator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)|  `QCTraceSimulator` |<span data-ttu-id="5a35c-125">Executa uma análise avançada de consumos de recursos para todo o grafo de chamadas do algoritmo e dá suporte a milhares de qubits.</span><span class="sxs-lookup"><span data-stu-id="5a35c-125">Runs advanced analysis of resources consumptions for the algorithm's entire call-graph, and supports thousands of qubits.</span></span>|
|[<span data-ttu-id="5a35c-126">Simulador do Toffoli</span><span class="sxs-lookup"><span data-stu-id="5a35c-126">Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)| `ToffoliSimulator` |<span data-ttu-id="5a35c-127">Simula os algoritmos quânticos que são limitados a `X`, `CNOT` e a operações quânticas `X` com vários controles e dá suporte a milhões de qubits.</span><span class="sxs-lookup"><span data-stu-id="5a35c-127">Simulates quantum algorithms that are limited to `X`, `CNOT`, and multi-controlled `X` quantum operations, and supports million of qubits.</span></span> |

## <a name="invoking-the-quantum-simulator"></a><span data-ttu-id="5a35c-128">Invocando o simulador quântico</span><span class="sxs-lookup"><span data-stu-id="5a35c-128">Invoking the quantum simulator</span></span>

<span data-ttu-id="5a35c-129">Em [Maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs), três modos de passar o código Q# para o simulador quântico são demonstrados:</span><span class="sxs-lookup"><span data-stu-id="5a35c-129">In [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs), three ways of passing the Q# code to the quantum simulator are demonstrated:</span></span> 

* <span data-ttu-id="5a35c-130">Usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="5a35c-130">Using the command line</span></span>
* <span data-ttu-id="5a35c-131">Usando um programa de host em Python</span><span class="sxs-lookup"><span data-stu-id="5a35c-131">Using a Python host program</span></span>
* <span data-ttu-id="5a35c-132">Usando um programa de host em C#</span><span class="sxs-lookup"><span data-stu-id="5a35c-132">Using a C# host program</span></span>

<span data-ttu-id="5a35c-133">Os computadores quânticos são instâncias de classes .NET normais e, portanto, são criadas invocando o construtor delas, assim como qualquer classe .NET.</span><span class="sxs-lookup"><span data-stu-id="5a35c-133">Quantum machines are instances of normal .NET classes, so they are created by invoking their constructor, just like any .NET class.</span></span> <span data-ttu-id="5a35c-134">O procedimento depende de como você executa o programa Q#.</span><span class="sxs-lookup"><span data-stu-id="5a35c-134">How you do this depends on how you run the Q# program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5a35c-135">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="5a35c-135">Next steps</span></span>

* <span data-ttu-id="5a35c-136">Para saber detalhes sobre como invocar computadores de destino para programas Q# em ambientes distintos, confira [Maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="5a35c-136">For details about how to invoke target machines for Q# programs in different environments, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
