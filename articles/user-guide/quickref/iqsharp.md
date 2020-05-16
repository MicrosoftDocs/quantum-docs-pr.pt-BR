---
title: Comandos magic do IQ#
description: 'Página de referência rápida para comandos mágicos de IQ # com o Q # Jupyter notebooks'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 0cd1a2289132e2760a21fd9d4f4083696353e271
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431012"
---
# <a name="iq-magic-commands"></a><span data-ttu-id="e7a3a-103">Comandos magic do IQ#</span><span class="sxs-lookup"><span data-stu-id="e7a3a-103">IQ# Magic Commands</span></span>

### <a name="general"></a><span data-ttu-id="e7a3a-104">Geral</span><span class="sxs-lookup"><span data-stu-id="e7a3a-104">General</span></span>

- <span data-ttu-id="e7a3a-105">`%config`: Define ou obtém as preferências de configuração.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-105">`%config`: Sets or gets configuration preferences.</span></span>
- <span data-ttu-id="e7a3a-106">`%estimate`: Executa uma determinada função ou operação no computador de destino QuantumSimulator.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-106">`%estimate`: Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="e7a3a-107">`%lsmagic`: Retorna uma lista de todos os comandos mágicos disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-107">`%lsmagic`: Returns a list of all currently available magic commands.</span></span>
- <span data-ttu-id="e7a3a-108">`%package`: Fornece a capacidade de carregar um pacote NuGet.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-108">`%package`: Provides the ability to load a Nuget package.</span></span>
- <span data-ttu-id="e7a3a-109">`%performance`: Relata as métricas de desempenho atuais para este kernel.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-109">`%performance`: Reports current performance metrics for this kernel.</span></span>
- <span data-ttu-id="e7a3a-110">`%simulate`: Executa uma determinada função ou operação no computador de destino QuantumSimulator.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-110">`%simulate`: Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="e7a3a-111">`%toffoli`: Executa uma determinada função ou operação no computador de destino do simulador de ToffoliSimulator.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-111">`%toffoli`: Runs a given function or operation on the ToffoliSimulator simulator target machine.</span></span>
- <span data-ttu-id="e7a3a-112">`%who`: Fornece ações relacionadas ao espaço de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-112">`%who`: Provides actions related to the current workspace.</span></span>
- <span data-ttu-id="e7a3a-113">`%workspace`: Retorna uma lista de todas as operações e funções definidas na sessão atual, interativamente ou carregadas do espaço de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-113">`%workspace`: Returns a list of all operations and functions defined in the current session, either interactively or loaded from the current workspace.</span></span>

### <a name="chemistry"></a><span data-ttu-id="e7a3a-114">Química</span><span class="sxs-lookup"><span data-stu-id="e7a3a-114">Chemistry</span></span>

- <span data-ttu-id="e7a3a-115">`%chemistry.broombridge`: Carrega e retorna a representação de problema de estrutura eletrônica Broombridge de um determinado arquivo. YAML.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-115">`%chemistry.broombridge`: Loads and returns Broombridge electronic structure problem representation from a given .yaml file.</span></span>
- <span data-ttu-id="e7a3a-116">`%chemistry.encode`: Codifica um Fermion Hamiltonian para um formato consumível por Q #.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-116">`%chemistry.encode`: Encodes a fermion Hamiltonian to a format consumable by Q#.</span></span>
- <span data-ttu-id="e7a3a-117">`%chemistry.fh.add_terms`: Adiciona termos a um Fermion Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-117">`%chemistry.fh.add_terms`: Adds terms to a fermion Hamiltonian.</span></span>
- <span data-ttu-id="e7a3a-118">`%chemistry.fh.load`: Carrega o Fermion Hamiltonian para um problema de estrutura eletrônica.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-118">`%chemistry.fh.load`: Loads the fermion Hamiltonian for an electronic structure problem.</span></span> <span data-ttu-id="e7a3a-119">O problema é carregado de um arquivo ou passado como um argumento.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-119">The problem is loaded from a file or passed as an argument.</span></span>
- <span data-ttu-id="e7a3a-120">`%chemistry.inputstate.load`: Carrega o problema de estrutura eletrônica do Broombridge e retorna o estado de entrada selecionado.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-120">`%chemistry.inputstate.load`: Loads Broombridge electronic structure problem and returns selected input state.</span></span>

### <a name="from-microsoftquantumkatas-package"></a><span data-ttu-id="e7a3a-121">Do pacote Microsoft. Quantum. katas</span><span class="sxs-lookup"><span data-stu-id="e7a3a-121">From Microsoft.Quantum.Katas package</span></span>

- <span data-ttu-id="e7a3a-122">`%kata`: Executa um único teste e relata se o teste foi aprovado com êxito.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-122">`%kata`: Executes a single test, and reports whether the test passed successfully.</span></span>
- <span data-ttu-id="e7a3a-123">`%check_kata`: Verifica a implementação de referência para um único teste de Kata.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-123">`%check_kata`: Checks the reference implementation for a single kata's test.</span></span>
    <span data-ttu-id="e7a3a-124">Especificamente, ele substitui a implementação de referência de uma única tarefa na célula e relata se o teste foi aprovado com êxito.</span><span class="sxs-lookup"><span data-stu-id="e7a3a-124">Specifically, it substitutes the reference implementation for a single task into the cell, and reports whether the test passed successfully.</span></span>
