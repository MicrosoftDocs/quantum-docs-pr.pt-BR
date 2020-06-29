---
title: Guia do usuário do Q#
description: Visão geral da finalidade e do conteúdo do guia do usuário
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
ms.openlocfilehash: c5611f3e2907791f2dfc1644be0a45515d50dfd7
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415348"
---
# <a name="the-q-user-guide"></a><span data-ttu-id="e6f34-103">Guia do usuário do Q#</span><span class="sxs-lookup"><span data-stu-id="e6f34-103">The Q# User Guide</span></span>

<span data-ttu-id="e6f34-104">Bem-vindo ao guia do usuário do Q#!</span><span class="sxs-lookup"><span data-stu-id="e6f34-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="e6f34-105">Nos diferentes tópicos deste guia, detalhamos os conceitos fundamentais da linguagem Q# e todas as informações de que você precisa para escrever programas quânticos.</span><span class="sxs-lookup"><span data-stu-id="e6f34-105">In the different topics of this guide, we detail the core concepts of the Q# language and all the information you need to write quantum programs.</span></span>

## <a name="user-guide-contents"></a><span data-ttu-id="e6f34-106">Conteúdo do guia do usuário</span><span class="sxs-lookup"><span data-stu-id="e6f34-106">User Guide Contents</span></span>

- <span data-ttu-id="e6f34-107">[Noções básicas da linguagem Q#](xref:microsoft.quantum.guide.basics): Uma visão geral introdutória da finalidade e da funcionalidade da linguagem de programação Q#.</span><span class="sxs-lookup"><span data-stu-id="e6f34-107">[Q# Basics](xref:microsoft.quantum.guide.basics): An introductory overview of the purpose and functionality of the Q# programming language.</span></span> 

### <a name="q-language"></a><span data-ttu-id="e6f34-108">Linguagem Q#</span><span class="sxs-lookup"><span data-stu-id="e6f34-108">Q# Language</span></span>

- <span data-ttu-id="e6f34-109">[Tipos em Q#](xref:microsoft.quantum.guide.types): Cria o modelo de tipo Q# e descreve a sintaxe para especificar e trabalhar com tipos.</span><span class="sxs-lookup"><span data-stu-id="e6f34-109">[Types in Q#](xref:microsoft.quantum.guide.types): Lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>

- <span data-ttu-id="e6f34-110">[Expressões de tipo](xref:microsoft.quantum.guide.expressions): Detalha como especificar, referenciar, combinar e operar em valores de cada tipo em Q#.</span><span class="sxs-lookup"><span data-stu-id="e6f34-110">[Type Expressions](xref:microsoft.quantum.guide.expressions): Details how to specify, reference, combine, and operate on values of each type in Q#.</span></span> 

### <a name="using-q"></a><span data-ttu-id="e6f34-111">Como usar o Q#</span><span class="sxs-lookup"><span data-stu-id="e6f34-111">Using Q#</span></span>

- <span data-ttu-id="e6f34-112">[Estrutura de arquivos Q#](xref:microsoft.quantum.guide.filestructure): Descreve a estrutura e a sintaxe de um arquivo `*.qs` Q#.</span><span class="sxs-lookup"><span data-stu-id="e6f34-112">[Q# File Structure](xref:microsoft.quantum.guide.filestructure): Describes the structure and syntax of a `*.qs` Q# file.</span></span>

- <span data-ttu-id="e6f34-113">[Operações e funções](xref:microsoft.quantum.guide.operationsfunctions): Detalha os dois tipos da linguagem Q# que podem ser chamados, isto é, *operações*, que incluem ação em registros qubit e *funções*, que funcionam estritamente com informações clássicas.</span><span class="sxs-lookup"><span data-stu-id="e6f34-113">[Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions): Details the two callable types of the Q# language: *operations*, which include action on qubit registers, and *functions*, which strictly work with classical information.</span></span> 
    <span data-ttu-id="e6f34-114">Aqui você verá como defini-los e chamá-los, incluindo as versões adjacentes e controladas de operadores quantum.</span><span class="sxs-lookup"><span data-stu-id="e6f34-114">Here you see how to define and call them, including the adjoint and controlled versions of quantum operations.</span></span>

- <span data-ttu-id="e6f34-115">[Variáveis](xref:microsoft.quantum.guide.variables): Descreve a função de variáveis em programas em Q# e como usá-las com eficiência.</span><span class="sxs-lookup"><span data-stu-id="e6f34-115">[Variables](xref:microsoft.quantum.guide.variables): Describes the role of variables within Q# programs and how to leverage them effectively.</span></span> 
    <span data-ttu-id="e6f34-116">Por exemplo, é possível encontrar informações sobre escopos de associação, bem como a diferença entre variáveis imutáveis e mutáveis e como atribuí-las ou reatribuí-las.</span><span class="sxs-lookup"><span data-stu-id="e6f34-116">For example, you can find information about binding scopes, as well as the difference between immutable and mutable variables and how to assign or re-assign them.</span></span>

- <span data-ttu-id="e6f34-117">[Trabalhar com qubits](xref:microsoft.quantum.guide.qubits): Descreve os recursos do Q # usados para tratar qubits e sistemas individuais do qubits, especificamente, alocando-os, executando operações neles e medindo-os.</span><span class="sxs-lookup"><span data-stu-id="e6f34-117">[Working with qubits](xref:microsoft.quantum.guide.qubits): Describes the features of Q# used to address individual qubits and systems of qubits, specifically, allocating them, performing operations on them, and measuring them.</span></span> 

- <span data-ttu-id="e6f34-118">[Fluxo de controle](xref:microsoft.quantum.guide.controlflow): Detalha os padrões do fluxo de controle de programação disponíveis no Q#, que inclui muitas técnicas padrão (como execução condicional, loops for, loops while etc.), bem como o padrão “Repeat-Until-Success” específico do quantum.</span><span class="sxs-lookup"><span data-stu-id="e6f34-118">[Control Flow](xref:microsoft.quantum.guide.controlflow): Details the programming control flow patterns available in Q#, which includes many standard techniques (such as conditional execution, for loops, while loops) as well as the quantum-specific "Repeat-Until-Success" pattern.</span></span>

- <span data-ttu-id="e6f34-119">[Testando e depurando](xref:microsoft.quantum.guide.testingdebugging): Detalha algumas técnicas para verificar se o código está fazendo o que deveria fazer.</span><span class="sxs-lookup"><span data-stu-id="e6f34-119">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): Details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="e6f34-120">Devido à opacidade geral das informações quânticas, a depuração de um programa quântico pode exigir técnicas especializadas.</span><span class="sxs-lookup"><span data-stu-id="e6f34-120">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="e6f34-121">Felizmente, o Q# dá suporte a muitas das técnicas de depuração clássicas com as quais os programadores estão familiarizados, bem como àquelas que são específicas para computação quântica.</span><span class="sxs-lookup"><span data-stu-id="e6f34-121">Fortunately, Q# supports many of the classical debugging techniques programmers are familiar with, as well as those that are quantum-specific.</span></span> <span data-ttu-id="e6f34-122">Isso inclui a criação e execução de testes de unidade em Q#, a inserção de *asserções* em valores e probabilidades em seu código e as funções de `Dump`, que produzem os estados dos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="e6f34-122">These include creating and running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the states of target machines.</span></span> 
    <span data-ttu-id="e6f34-123">Essas últimas podem ser usadas junto com nosso simulador de estado completo para depurar determinadas partes de computações contornando algumas limitações da computação quântica (por exemplo, o [teorema da não clonagem](xref:microsoft.quantum.concepts.pauli)).</span><span class="sxs-lookup"><span data-stu-id="e6f34-123">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations, for example, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="e6f34-124">Simuladores Quantum e avaliadores de recursos</span><span class="sxs-lookup"><span data-stu-id="e6f34-124">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="e6f34-125">[Simuladores e aplicativos host quânticos](xref:microsoft.quantum.machines): Uma visão geral dos diferentes simuladores disponíveis, bem como o modelo de execução geral entre os programas host e os computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="e6f34-125">[Quantum simulators and host applications](xref:microsoft.quantum.machines): An overview of the different simulators available, as well as the general execution model between host programs and target machines.</span></span>

- <span data-ttu-id="e6f34-126">[Simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator): O computador de destino que simula o estado quântico completo.</span><span class="sxs-lookup"><span data-stu-id="e6f34-126">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): The target machine which simulates the full quantum state.</span></span> <span data-ttu-id="e6f34-127">Útil para execução ou depuração completa de programas de menor escala (menos que algumas dúzias de qubits)</span><span class="sxs-lookup"><span data-stu-id="e6f34-127">Useful for fully executing or debugging smaller-scale programs (less than a few dozen qubits)</span></span>

- <span data-ttu-id="e6f34-128">[Estimador de recursos](xref:microsoft.quantum.machines.resources-estimator): Estima os recursos necessários para executar uma determinada instância de uma operação em Q# em um computador quantum.</span><span class="sxs-lookup"><span data-stu-id="e6f34-128">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): Estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="e6f34-129">[Simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Executa um programa quantum da Microsoft sem realmente simular o estado de um computador quantum e, portanto, pode executar programas quantum que usam milhares de qubits.</span><span class="sxs-lookup"><span data-stu-id="e6f34-129">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Executes a quantum program without actually simulating the state of a quantum computer, and therefore can execute quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="e6f34-130">Útil para depurar um código clássico dentro de um programa quantum, bem como estimar os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="e6f34-130">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="e6f34-131">[Simulador do Toffoli](xref:microsoft.quantum.machines.toffoli-simulator): Um simulador quantum de uso especial que pode ser usado com milhões de qubits, mas somente para programas com um conjunto restrito de operações quantum (X, CNOT e X multicontrolado).</span><span class="sxs-lookup"><span data-stu-id="e6f34-131">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): A special-purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations - X, CNOT, and multi-controlled X.</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="e6f34-132">Páginas de referência rápida</span><span class="sxs-lookup"><span data-stu-id="e6f34-132">Quick Reference Pages</span></span>

- <span data-ttu-id="e6f34-133">[Comandos magic do IQ#](xref:microsoft.quantum.guide.quickref.iqsharp): Página de referência rápida para comandos magic do IQ# Jupyter Notebooks em Q#.</span><span class="sxs-lookup"><span data-stu-id="e6f34-133">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
