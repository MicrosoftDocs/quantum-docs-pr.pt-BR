---
title: Guia do usuário do Q#
description: Visão geral da finalidade e do conteúdo do guia do usuário
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
ms.openlocfilehash: f535aaedbe6ce181375d48f7023409ad8212c702
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430604"
---
# <a name="the-q-user-guide"></a><span data-ttu-id="6f9b8-103">Guia do usuário do Q#</span><span class="sxs-lookup"><span data-stu-id="6f9b8-103">The Q# User Guide</span></span>

<span data-ttu-id="6f9b8-104">Bem-vindo ao guia do usuário do Q#!</span><span class="sxs-lookup"><span data-stu-id="6f9b8-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="6f9b8-105">Aqui detalhamos os conceitos fundamentais da linguagem Q# e todas as informações de que você precisa para escrever programas quânticos.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-105">Here we detail the core concepts of the Q# language and all the information you need to write quantum programs.</span></span>

## <a name="user-guide-contents"></a><span data-ttu-id="6f9b8-106">Conteúdo do guia do usuário</span><span class="sxs-lookup"><span data-stu-id="6f9b8-106">User Guide Contents</span></span>

- <span data-ttu-id="6f9b8-107">[Noções básicas do Q#](xref:microsoft.quantum.guide.basics): uma visão geral introdutória da finalidade e da funcionalidade da linguagem de programação Q#.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-107">[Q# Basics](xref:microsoft.quantum.guide.basics): an introductory overview of the purpose and functionality of the Q# programming language.</span></span> 

### <a name="q-language"></a><span data-ttu-id="6f9b8-108">Linguagem Q#</span><span class="sxs-lookup"><span data-stu-id="6f9b8-108">Q# Language</span></span>

- <span data-ttu-id="6f9b8-109">[Tipos em Q#](xref:microsoft.quantum.guide.types): cria o modelo de tipo Q# e descreve a sintaxe para especificar e trabalhar com tipos.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-109">[Types in Q#](xref:microsoft.quantum.guide.types): lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>

- <span data-ttu-id="6f9b8-110">[Expressões de tipo](xref:microsoft.quantum.guide.expressions): detalha como especificar, referenciar, combinar e operar em valores de cada tipo em Q#.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-110">[Type Expressions](xref:microsoft.quantum.guide.expressions): details how to specify, reference, combine, and operate on values of each type in Q#.</span></span> 

### <a name="using-q"></a><span data-ttu-id="6f9b8-111">Como usar o Q#</span><span class="sxs-lookup"><span data-stu-id="6f9b8-111">Using Q#</span></span>

- <span data-ttu-id="6f9b8-112">[Estrutura de arquivos Q#](xref:microsoft.quantum.guide.filestructure): descreve a estrutura e a sintaxe de um arquivo `*.qs` Q#.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-112">[Q# File Structure](xref:microsoft.quantum.guide.filestructure): describes the structure and syntax of a `*.qs` Q# file.</span></span>

- <span data-ttu-id="6f9b8-113">[Operações e funções](xref:microsoft.quantum.guide.operationsfunctions): detalha os dois tipos da linguagem Q# que podem ser chamados, isto é, *operações*, que incluem ação em registros qubit, e *funções*, que funcionam estritamente com informações clássicas.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-113">[Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions): details the two callable types of the Q# language: *operations*, which include action on qubit registers and *functions*, which strictly work with classical information.</span></span> 
    <span data-ttu-id="6f9b8-114">Aqui você verá como defini-los e chamá-los, incluindo as versões adjacentes e controladas de operadores quantum.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-114">Here you see how to define and call them, including the adjoint and controlled versions of quantum operations.</span></span>

- <span data-ttu-id="6f9b8-115">[Variáveis](xref:microsoft.quantum.guide.variables): descreve a função de variáveis em programas em Q# e como usá-las com eficiência.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-115">[Variables](xref:microsoft.quantum.guide.variables): describes the role of variables within Q# programs and how to leverage them effectively.</span></span> 
    <span data-ttu-id="6f9b8-116">Por exemplo, é possível encontrar informações sobre escopos de associação, bem como a diferença entre variáveis imutáveis/mutáveis e como atribuí-las/reatribuí-las.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-116">For example, you can find information about binding scopes, as well as the difference between immutable/mutable variables and how to assign/re-assign them.</span></span>

- <span data-ttu-id="6f9b8-117">[Trabalhar com qubits](xref:microsoft.quantum.guide.qubits): descreve os recursos do Q# usados para lidar com qubits individuais e sistemas de qubits.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-117">[Working with qubits](xref:microsoft.quantum.guide.qubits): describes the features of Q# used to address individual qubits and systems of qubits.</span></span> 
    <span data-ttu-id="6f9b8-118">Especificamente, isso envolve a alocação e a medição desses qubits, bem como a execução de operações neles.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-118">Specifically, that entails their allocation, performing operations on them, and ultimately their measurement.</span></span> 

- <span data-ttu-id="6f9b8-119">[Fluxo de controle](xref:microsoft.quantum.guide.controlflow): detalha os padrões do fluxo de controle de programação disponíveis no Q#, que inclui muitas técnicas padrão (execução condicional, loops for, loops while etc.), bem como o padrão “Repeat-Until-Success” específico do quantum.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-119">[Control Flow](xref:microsoft.quantum.guide.controlflow): details the programming control flow patterns available in Q#, which includes many standard techniques (conditional execution, for loops, while loops, etc.) as well as the quantum-specific "Repeat-Until-Success" pattern.</span></span>

- <span data-ttu-id="6f9b8-120">[Teste e depuração](xref:microsoft.quantum.guide.testingdebugging): detalha algumas técnicas para verificar se o código está fazendo o que deveria fazer.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-120">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="6f9b8-121">Devido à opacidade geral das informações quânticas, a depuração de um programa quântico pode exigir técnicas especializadas.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-121">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="6f9b8-122">Felizmente, o Q# dá suporte a muitas das técnicas de depuração clássicas com as quais os programadores estão acostumados, bem como àquelas que são específicas para computação quântica.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-122">Fortunately, Q# supports many of the classical debugging techniques programmers are used to, as well as those that are quantum-specific.</span></span> <span data-ttu-id="6f9b8-123">Isso inclui a criação/execução de testes de unidade em Q#, a inserção de *asserções* em valores e probabilidades em seu código e as funções de `Dump`, que produzem o estado do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-123">These include creating/running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the state of target machine.</span></span> 
    <span data-ttu-id="6f9b8-124">Essas últimas podem ser usadas junto com nosso simulador de estado completo para depurar determinadas partes de computações contornando algumas limitações da computação quântica (por exemplo, o teorema da não clonagem).</span><span class="sxs-lookup"><span data-stu-id="6f9b8-124">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations (e.g. the no-cloning theorem).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="6f9b8-125">Simuladores Quantum e avaliadores de recursos</span><span class="sxs-lookup"><span data-stu-id="6f9b8-125">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="6f9b8-126">[Simuladores quantum e aplicativos host](xref:microsoft.quantum.machines): uma visão geral dos diferentes simuladores disponíveis, bem como o modelo de execução geral entre o programa host e os computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-126">[Quantum simulators and host applications](xref:microsoft.quantum.machines): an overview of the different simulators available, as well as the general execution model between host program and target machines.</span></span>

- <span data-ttu-id="6f9b8-127">[Simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator): o computador de destino que simula o estado quântico completo.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-127">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): the target machine which simulates the full quantum state.</span></span> <span data-ttu-id="6f9b8-128">Útil para execução ou depuração completa de programas de menor escala (menos de duas dúzias de qubits)</span><span class="sxs-lookup"><span data-stu-id="6f9b8-128">Useful for fully executing or debugging smaller scale programs (less than a couple dozen qubits)</span></span>

- <span data-ttu-id="6f9b8-129">[Avaliador de recursos](xref:microsoft.quantum.machines.resources-estimator): estima os recursos necessários para executar uma determinada instância de uma operação em Q# em um computador quantum.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-129">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="6f9b8-130">[Simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro): executa um programa quantum da Microsoft sem realmente simular o estado de um computador quantum e, portanto, pode executar programas quantum que usam milhares de qubits.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-130">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): executes a quantum program without actually simulating the state of a quantum computer, and therefore can execute quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="6f9b8-131">Útil para depurar um código clássico dentro de um programa quantum, bem como estimar os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-131">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="6f9b8-132">[Simulador Toffoli](xref:microsoft.quantum.machines.toffoli-simulator): um simulador quantum de uso especial que pode ser usado com milhões de qubits, mas somente para programas com um conjunto restrito de operações quantum (ou seja, X, CNOT e X com vários controlados).</span><span class="sxs-lookup"><span data-stu-id="6f9b8-132">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): a special purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations (namely X, CNOT, and multi-controlled X).</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="6f9b8-133">Páginas de referência rápida</span><span class="sxs-lookup"><span data-stu-id="6f9b8-133">Quick Reference Pages</span></span>

- <span data-ttu-id="6f9b8-134">[Comandos magic do IQ#](xref:microsoft.quantum.guide.quickref.iqsharp): Página de referência rápida para comandos magic do IQ# Jupyter Notebooks em Q#.</span><span class="sxs-lookup"><span data-stu-id="6f9b8-134">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
