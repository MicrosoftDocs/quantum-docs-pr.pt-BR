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
ms.openlocfilehash: 979e468cc743bd9125eaba0b71f794977c914447
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231750"
---
# <a name="the-no-locq-user-guide"></a><span data-ttu-id="c33f4-103">Guia do usuário do Q#</span><span class="sxs-lookup"><span data-stu-id="c33f4-103">The Q# User Guide</span></span>

<span data-ttu-id="c33f4-104">Bem-vindo(a) ao guia do usuário do Q#!</span><span class="sxs-lookup"><span data-stu-id="c33f4-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="c33f4-105">Nos diferentes tópicos deste guia, apresentamos algumas das noções básicas para o desenvolvimento de programas quantum usando o Q#.</span><span class="sxs-lookup"><span data-stu-id="c33f4-105">In the different topics of this guide, we introduce some of the basics for developing quantum programs using Q#.</span></span>

<span data-ttu-id="c33f4-106">Nós nos referimos ao guia da linguagem [Q#](xref:microsoft.quantum.qsharp.index) para obter uma especificação e documentação completas da linguagem de programação quantum Q#.</span><span class="sxs-lookup"><span data-stu-id="c33f4-106">We refer to the [Q# language guide](xref:microsoft.quantum.qsharp.index) for a full specification and documentation of the Q# quantum programming language.</span></span> 

## <a name="user-guide-contents"></a><span data-ttu-id="c33f4-107">Conteúdo do guia do usuário</span><span class="sxs-lookup"><span data-stu-id="c33f4-107">User Guide Contents</span></span>

- <span data-ttu-id="c33f4-108">Programas [Q#](xref:microsoft.quantum.guide.programs): uma rápida introdução aos programas quânticos no Q#.</span><span class="sxs-lookup"><span data-stu-id="c33f4-108">[Q# programs](xref:microsoft.quantum.guide.programs): An quick introduction to quantum programs in Q#.</span></span> 

- <span data-ttu-id="c33f4-109">[Maneiras de executar um programa Q#](xref:microsoft.quantum.guide.host-programs): descreve como um programa Q# é executado e mostra uma visão geral das diversas formas de chamar o programa: da linha de comando, de Jupyter Notebooks Q# ou de um programa de host clássico escrito em uma linguagem Python ou .NET.</span><span class="sxs-lookup"><span data-stu-id="c33f4-109">[Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs): describes how a Q# program is run, and provides an overview of the various ways you can call the program: from the command line, in Q# Jupyter Notebooks, or from a classical host program written in Python or a .NET language.</span></span>

- <span data-ttu-id="c33f4-110">[Testando e depurando](xref:microsoft.quantum.guide.testingdebugging): Detalha algumas técnicas para verificar se o código está fazendo o que deveria fazer.</span><span class="sxs-lookup"><span data-stu-id="c33f4-110">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): Details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="c33f4-111">Devido à opacidade geral das informações quânticas, a depuração de um programa quântico pode exigir técnicas especializadas.</span><span class="sxs-lookup"><span data-stu-id="c33f4-111">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="c33f4-112">Felizmente, o Q# é compatível com muitas das técnicas de depuração clássicas que os programadores já conhecem, bem como aquelas específicas para computação quântica.</span><span class="sxs-lookup"><span data-stu-id="c33f4-112">Fortunately, Q# supports many of the classical debugging techniques programmers are familiar with, as well as those that are quantum-specific.</span></span> <span data-ttu-id="c33f4-113">Isso inclui a criação e execução de testes de unidade em Q#, a inserção de *declarações* em valores e probabilidades no código e as funções `Dump`, que produzem os estados dos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="c33f4-113">These include creating and running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the states of target machines.</span></span> 
    <span data-ttu-id="c33f4-114">Essas últimas podem ser usadas junto com nosso simulador de estado completo para depurar determinadas partes de computações contornando algumas limitações da computação quântica (por exemplo, o [teorema da não clonagem](xref:microsoft.quantum.concepts.pauli)).</span><span class="sxs-lookup"><span data-stu-id="c33f4-114">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations, for example, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="c33f4-115">Simuladores Quantum e avaliadores de recursos</span><span class="sxs-lookup"><span data-stu-id="c33f4-115">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="c33f4-116">[Simuladores e aplicativos host quânticos](xref:microsoft.quantum.machines): Uma visão geral dos diferentes simuladores disponíveis e de como os programas host e os computadores de destino funcionam juntos para executar programas Q#.</span><span class="sxs-lookup"><span data-stu-id="c33f4-116">[Quantum simulators and host applications](xref:microsoft.quantum.machines): An overview of the different simulators available, as well of how host programs and target machines work together to run Q# programs.</span></span>

- <span data-ttu-id="c33f4-117">[Simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator): O computador de destino que simula o estado quântico completo.</span><span class="sxs-lookup"><span data-stu-id="c33f4-117">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): The target machine which simulates the full quantum state.</span></span> <span data-ttu-id="c33f4-118">Útil para execução ou depuração completa de programas de menor escala (menos que algumas dúzias de qubits)</span><span class="sxs-lookup"><span data-stu-id="c33f4-118">Useful for fully running or debugging smaller-scale programs (less than a few dozen qubits)</span></span>

- <span data-ttu-id="c33f4-119">[Estimador de recursos](xref:microsoft.quantum.machines.resources-estimator): Estima os recursos necessários para executar uma determinada instância de uma operação em Q# em um computador quântico.</span><span class="sxs-lookup"><span data-stu-id="c33f4-119">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): Estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="c33f4-120">[Simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Executa um programa quântico da Microsoft sem realmente simular o estado de um computador quântico e, portanto, pode executar programas quânticos que usam milhares de qubits.</span><span class="sxs-lookup"><span data-stu-id="c33f4-120">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Runs a quantum program without actually simulating the state of a quantum computer, and therefore can run quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="c33f4-121">Útil para depurar um código clássico dentro de um programa quantum, bem como estimar os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="c33f4-121">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="c33f4-122">[Simulador do Toffoli](xref:microsoft.quantum.machines.toffoli-simulator): Um simulador quantum de uso especial que pode ser usado com milhões de qubits, mas somente para programas com um conjunto restrito de operações quantum (X, CNOT e X multicontrolado).</span><span class="sxs-lookup"><span data-stu-id="c33f4-122">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): A special-purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations - X, CNOT, and multi-controlled X.</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="c33f4-123">Páginas de referência rápida</span><span class="sxs-lookup"><span data-stu-id="c33f4-123">Quick Reference Pages</span></span>

- <span data-ttu-id="c33f4-124">Comandos magic do [IQ#](xref:microsoft.quantum.guide.quickref.iqsharp): Página de referência rápida para comandos magic do IQ# do Jupyter Notebooks no Q#.</span><span class="sxs-lookup"><span data-stu-id="c33f4-124">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
