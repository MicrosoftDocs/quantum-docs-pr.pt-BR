---
title: Guia do usuário do Q#
description: Visão geral da finalidade e do conteúdo do guia do usuário
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
no-loc:
- Q#
- $$v
ms.openlocfilehash: f0680e773c8233d6c4f1acb742b3cc38dbc069d5
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834747"
---
# <a name="the-no-locq-user-guide"></a><span data-ttu-id="35b84-103">Guia do usuário do Q#</span><span class="sxs-lookup"><span data-stu-id="35b84-103">The Q# User Guide</span></span>

<span data-ttu-id="35b84-104">Bem-vindo(a) ao guia do usuário do Q#!</span><span class="sxs-lookup"><span data-stu-id="35b84-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="35b84-105">Nos diferentes tópicos deste guia, detalhamos os conceitos fundamentais da linguagem Q# e todas as informações de que você precisa para escrever programas quânticos.</span><span class="sxs-lookup"><span data-stu-id="35b84-105">In the different topics of this guide, we detail the core concepts of the Q# language and all the information you need to write quantum programs.</span></span>

## <a name="user-guide-contents"></a><span data-ttu-id="35b84-106">Conteúdo do guia do usuário</span><span class="sxs-lookup"><span data-stu-id="35b84-106">User Guide Contents</span></span>

- <span data-ttu-id="35b84-107">[Q# Noções básicas](xref:microsoft.quantum.guide.basics): Uma visão geral introdutória da finalidade e da funcionalidade da linguagem de programação Q#.</span><span class="sxs-lookup"><span data-stu-id="35b84-107">[Q# Basics](xref:microsoft.quantum.guide.basics): An introductory overview of the purpose and functionality of the Q# programming language.</span></span> 

- <span data-ttu-id="35b84-108">[Maneiras de executar um programa Q#](xref:microsoft.quantum.guide.host-programs): descreve como um programa Q# é executado e mostra uma visão geral das diversas formas de chamar o programa: da linha de comando, de Jupyter Notebooks Q# ou de um programa de host clássico escrito em uma linguagem Python ou .NET.</span><span class="sxs-lookup"><span data-stu-id="35b84-108">[Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs): describes how a Q# program is run, and provides an overview of the various ways you can call the program: from the command line, in Q# Jupyter Notebooks, or from a classical host program written in Python or a .NET language.</span></span>

### <a name="no-locq-language"></a><span data-ttu-id="35b84-109">Linguagem Q#</span><span class="sxs-lookup"><span data-stu-id="35b84-109">Q# Language</span></span>

- <span data-ttu-id="35b84-110">[Tipos no Q#](xref:microsoft.quantum.guide.types): Cria o modelo de tipo Q# e descreve a sintaxe para especificar e trabalhar com tipos.</span><span class="sxs-lookup"><span data-stu-id="35b84-110">[Types in Q#](xref:microsoft.quantum.guide.types): Lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>

- <span data-ttu-id="35b84-111">[Expressões de tipo](xref:microsoft.quantum.guide.expressions): Detalha como especificar, referenciar, combinar e operar em valores de cada tipo em Q#.</span><span class="sxs-lookup"><span data-stu-id="35b84-111">[Type Expressions](xref:microsoft.quantum.guide.expressions): Details how to specify, reference, combine, and operate on values of each type in Q#.</span></span> 

### <a name="using-no-locq"></a><span data-ttu-id="35b84-112">Usando Q#</span><span class="sxs-lookup"><span data-stu-id="35b84-112">Using Q#</span></span>

- <span data-ttu-id="35b84-113">[Q# Estrutura do arquivo](xref:microsoft.quantum.guide.filestructure): Descreve a estrutura e a sintaxe de um arquivo `*.qs` no Q#.</span><span class="sxs-lookup"><span data-stu-id="35b84-113">[Q# File Structure](xref:microsoft.quantum.guide.filestructure): Describes the structure and syntax of a `*.qs` Q# file.</span></span>

- <span data-ttu-id="35b84-114">[Operações e funções](xref:microsoft.quantum.guide.operationsfunctions): Detalha os dois tipos da linguagem Q# que podem ser chamados: *operações*, que incluem ação em registros qubit, e *funções*, que funcionam estritamente com informações clássicas.</span><span class="sxs-lookup"><span data-stu-id="35b84-114">[Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions): Details the two callable types of the Q# language: *operations*, which include action on qubit registers, and *functions*, which strictly work with classical information.</span></span> 
    <span data-ttu-id="35b84-115">Aqui você verá como defini-los e chamá-los, incluindo as versões adjacentes e controladas de operadores quantum.</span><span class="sxs-lookup"><span data-stu-id="35b84-115">Here you see how to define and call them, including the adjoint and controlled versions of quantum operations.</span></span>

- <span data-ttu-id="35b84-116">[Variáveis](xref:microsoft.quantum.guide.variables): Descreve a função de variáveis em programas Q# e como usá-las com eficiência.</span><span class="sxs-lookup"><span data-stu-id="35b84-116">[Variables](xref:microsoft.quantum.guide.variables): Describes the role of variables within Q# programs and how to leverage them effectively.</span></span> 
    <span data-ttu-id="35b84-117">Por exemplo, é possível encontrar informações sobre escopos de associação, bem como a diferença entre variáveis imutáveis e mutáveis e como atribuí-las ou reatribuí-las.</span><span class="sxs-lookup"><span data-stu-id="35b84-117">For example, you can find information about binding scopes, as well as the difference between immutable and mutable variables and how to assign or re-assign them.</span></span>

- <span data-ttu-id="35b84-118">[Trabalhar com qubits](xref:microsoft.quantum.guide.qubits): Descreve os recursos do Q# usados para tratar qubits e sistemas individuais do qubits, especificamente, alocando-os, executando operações neles e medindo-os.</span><span class="sxs-lookup"><span data-stu-id="35b84-118">[Working with qubits](xref:microsoft.quantum.guide.qubits): Describes the features of Q# used to address individual qubits and systems of qubits, specifically, allocating them, performing operations on them, and measuring them.</span></span> 

- <span data-ttu-id="35b84-119">[Fluxo de controle](xref:microsoft.quantum.guide.controlflow): Detalha os padrões do fluxo de controle de programação disponíveis no Q#, que incluem muitas técnicas padrão (como processamento condicional, loops *for* e loops *while*), bem como o padrão *Repeat-Until-Success* específico da computação quântica.</span><span class="sxs-lookup"><span data-stu-id="35b84-119">[Control Flow](xref:microsoft.quantum.guide.controlflow): Details the programming control flow patterns available in Q#, which includes many standard techniques (such as conditional processing, *for* loops, *while* loops) as well as the quantum-specific *Repeat-Until-Success* pattern.</span></span>

- <span data-ttu-id="35b84-120">[Testando e depurando](xref:microsoft.quantum.guide.testingdebugging): Detalha algumas técnicas para verificar se o código está fazendo o que deveria fazer.</span><span class="sxs-lookup"><span data-stu-id="35b84-120">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): Details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="35b84-121">Devido à opacidade geral das informações quânticas, a depuração de um programa quântico pode exigir técnicas especializadas.</span><span class="sxs-lookup"><span data-stu-id="35b84-121">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="35b84-122">Felizmente, o Q# é compatível com muitas das técnicas de depuração clássicas que os programadores já conhecem, bem como aquelas específicas para computação quântica.</span><span class="sxs-lookup"><span data-stu-id="35b84-122">Fortunately, Q# supports many of the classical debugging techniques programmers are familiar with, as well as those that are quantum-specific.</span></span> <span data-ttu-id="35b84-123">Isso inclui a criação e execução de testes de unidade em Q#, a inserção de *declarações* em valores e probabilidades no código e as funções `Dump`, que produzem os estados dos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="35b84-123">These include creating and running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the states of target machines.</span></span> 
    <span data-ttu-id="35b84-124">Essas últimas podem ser usadas junto com nosso simulador de estado completo para depurar determinadas partes de computações contornando algumas limitações da computação quântica (por exemplo, o [teorema da não clonagem](xref:microsoft.quantum.concepts.pauli)).</span><span class="sxs-lookup"><span data-stu-id="35b84-124">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations, for example, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="35b84-125">Simuladores Quantum e avaliadores de recursos</span><span class="sxs-lookup"><span data-stu-id="35b84-125">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="35b84-126">[Simuladores e aplicativos host quânticos](xref:microsoft.quantum.machines): Uma visão geral dos diferentes simuladores disponíveis, bem como o modelo de execução geral entre os programas host e os computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="35b84-126">[Quantum simulators and host applications](xref:microsoft.quantum.machines): An overview of the different simulators available, as well as the general run model between host programs and target machines.</span></span>

- <span data-ttu-id="35b84-127">[Simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator): O computador de destino que simula o estado quântico completo.</span><span class="sxs-lookup"><span data-stu-id="35b84-127">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): The target machine which simulates the full quantum state.</span></span> <span data-ttu-id="35b84-128">Útil para execução ou depuração completa de programas de menor escala (menos que algumas dúzias de qubits)</span><span class="sxs-lookup"><span data-stu-id="35b84-128">Useful for fully running or debugging smaller-scale programs (less than a few dozen qubits)</span></span>

- <span data-ttu-id="35b84-129">[Estimador de recursos](xref:microsoft.quantum.machines.resources-estimator): Estima os recursos necessários para executar uma determinada instância de uma operação em Q# em um computador quântico.</span><span class="sxs-lookup"><span data-stu-id="35b84-129">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): Estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="35b84-130">[Simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Executa um programa quântico da Microsoft sem realmente simular o estado de um computador quântico e, portanto, pode executar programas quânticos que usam milhares de qubits.</span><span class="sxs-lookup"><span data-stu-id="35b84-130">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Runs a quantum program without actually simulating the state of a quantum computer, and therefore can run quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="35b84-131">Útil para depurar um código clássico dentro de um programa quantum, bem como estimar os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="35b84-131">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="35b84-132">[Simulador do Toffoli](xref:microsoft.quantum.machines.toffoli-simulator): Um simulador quantum de uso especial que pode ser usado com milhões de qubits, mas somente para programas com um conjunto restrito de operações quantum (X, CNOT e X multicontrolado).</span><span class="sxs-lookup"><span data-stu-id="35b84-132">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): A special-purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations - X, CNOT, and multi-controlled X.</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="35b84-133">Páginas de referência rápida</span><span class="sxs-lookup"><span data-stu-id="35b84-133">Quick Reference Pages</span></span>

- <span data-ttu-id="35b84-134">Comandos magic do [IQ#](xref:microsoft.quantum.guide.quickref.iqsharp): Página de referência rápida para comandos magic do IQ# do Jupyter Notebooks no Q#.</span><span class="sxs-lookup"><span data-stu-id="35b84-134">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
