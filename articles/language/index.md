---
title: A linguagem de programação Q#
description: Introdução à linguagem Q# para desenvolvimento de programa quântico.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.intro
ms.openlocfilehash: b62e6866fc3609d95c26a5eab2a6eac325dfe330
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907368"
---
# <a name="the-q-programming-language"></a><span data-ttu-id="739c8-103">A linguagem de programação Q#</span><span class="sxs-lookup"><span data-stu-id="739c8-103">The Q# Programming Language</span></span>

## <a name="introduction"></a><span data-ttu-id="739c8-104">Introdução</span><span class="sxs-lookup"><span data-stu-id="739c8-104">Introduction</span></span>

<span data-ttu-id="739c8-105">Um modelo natural para a computação quântica é tratar o computador quântico como um coprocessador, semelhante àquele usado para GPUs, FPGAs e outros processadores suplementares.</span><span class="sxs-lookup"><span data-stu-id="739c8-105">A natural model for quantum computation is to treat the quantum computer as a coprocessor, similar to that used for GPUs, FPGAs, and other adjunct processors.</span></span>
<span data-ttu-id="739c8-106">A lógica de controle principal executa o código clássico em um computador "host" clássico.</span><span class="sxs-lookup"><span data-stu-id="739c8-106">The primary control logic runs classical code on a classical "host" computer.</span></span>
<span data-ttu-id="739c8-107">Quando apropriado e necessário, o programa host pode invocar uma sub-rotina que é executada no processador suplementar.</span><span class="sxs-lookup"><span data-stu-id="739c8-107">When appropriate and necessary, the host program can invoke a subroutine that runs on the adjunct processor.</span></span>
<span data-ttu-id="739c8-108">Quando a sub-rotina é concluída, o programa host obtém acesso aos resultados da sub-rotina.</span><span class="sxs-lookup"><span data-stu-id="739c8-108">When the subroutine completes, the host program gets access to the subroutine's results.</span></span>

<span data-ttu-id="739c8-109">O Q# (Q-Sharp) é uma linguagem de programação específica de domínio usada para expressar algoritmos quânticos.</span><span class="sxs-lookup"><span data-stu-id="739c8-109">Q# (Q-sharp) is a domain-specific programming language used for expressing quantum algorithms.</span></span>
<span data-ttu-id="739c8-110">Ele deve ser usado para escrever sub-rotinas que são executadas em um processador quântico suplementar, sob o controle de um programa e um computador host clássico.</span><span class="sxs-lookup"><span data-stu-id="739c8-110">It is to be used for writing subroutines that execute on an adjunct quantum processor, under the control of a classical host program and computer.</span></span>
<span data-ttu-id="739c8-111">Até que os processadores quânticos estejam amplamente disponíveis, as sub-rotinas Q# são executadas em um simulador.</span><span class="sxs-lookup"><span data-stu-id="739c8-111">Until quantum processors are widely available, Q# subroutines execute on a simulator.</span></span>

<span data-ttu-id="739c8-112">O Q# fornece um pequeno conjunto de tipos primitivos, juntamente com duas maneiras (matrizes e tuplas) de criar tipos estruturados.</span><span class="sxs-lookup"><span data-stu-id="739c8-112">Q# provides a small set of primitive types, along with two ways (arrays and tuples) for creating new, structured types.</span></span>
<span data-ttu-id="739c8-113">Ele dá suporte a um modelo de procedimento básico para escrever programas, com loops e instruções if/then.</span><span class="sxs-lookup"><span data-stu-id="739c8-113">It supports a basic procedural model for writing programs, with loops and if/then statements.</span></span>
<span data-ttu-id="739c8-114">Os constructos de nível superior no Q# são operações, funções e tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="739c8-114">The top-level constructs in Q# are user defined types, operations, and functions.</span></span>

<span data-ttu-id="739c8-115">As seguintes seções fornecem detalhes sobre:</span><span class="sxs-lookup"><span data-stu-id="739c8-115">The following sections detail:</span></span>
- [<span data-ttu-id="739c8-116">O modelo de tipo</span><span class="sxs-lookup"><span data-stu-id="739c8-116">The Type Model</span></span>](xref:microsoft.quantum.language.type-model)
- [<span data-ttu-id="739c8-117">Expressões</span><span class="sxs-lookup"><span data-stu-id="739c8-117">Expressions</span></span>](xref:microsoft.quantum.language.expressions)
- [<span data-ttu-id="739c8-118">Instruções</span><span class="sxs-lookup"><span data-stu-id="739c8-118">Statements</span></span>](xref:microsoft.quantum.language.statements)
- [<span data-ttu-id="739c8-119">Estrutura do arquivo</span><span class="sxs-lookup"><span data-stu-id="739c8-119">File Structure</span></span>](xref:microsoft.quantum.language.file-structure)

## <a name="conventions"></a><span data-ttu-id="739c8-120">Convenções</span><span class="sxs-lookup"><span data-stu-id="739c8-120">Conventions</span></span>

<span data-ttu-id="739c8-121">Estamos trabalhando para garantir que sinais de pontuação comuns sejam usados de forma consistente em todas as situações.</span><span class="sxs-lookup"><span data-stu-id="739c8-121">We are working to ensure that common punctuation marks are used consistently in all situations.</span></span>
<span data-ttu-id="739c8-122">Esperamos que isso torne o Q# mais fácil de ser aprendido e lido, pois esses sinais sempre significam a mesma coisa e o mesmo conceito é sempre representado da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="739c8-122">We expect that this will make Q# easier to learn and to read because these marks always mean the same thing, and the same concept is always represented the same way.</span></span>

<span data-ttu-id="739c8-123">Especificamente:</span><span class="sxs-lookup"><span data-stu-id="739c8-123">Specifically:</span></span>

- <span data-ttu-id="739c8-124">O ponto e vírgula, `;`, é usado para encerrar uma instrução ou uma diretiva de linha única.</span><span class="sxs-lookup"><span data-stu-id="739c8-124">The semi-colon, `;`, is used to end a statement or single-line directive.</span></span>
  <span data-ttu-id="739c8-125">Ele não pode ser usado para nenhuma outra finalidade.</span><span class="sxs-lookup"><span data-stu-id="739c8-125">It is not used for any other purpose.</span></span>
- <span data-ttu-id="739c8-126">A vírgula, `,`, é usada para separar elementos de uma sequência.</span><span class="sxs-lookup"><span data-stu-id="739c8-126">The comma, `,`, is used to separate elements of a sequence.</span></span> <span data-ttu-id="739c8-127">Ela é usada para literais de tupla, literais de matriz, listas de argumentos, definições de tupla e listas de tipos.</span><span class="sxs-lookup"><span data-stu-id="739c8-127">It is used for tuple literals, array literals, argument lists, tuple definitions, and type lists.</span></span> <span data-ttu-id="739c8-128">**Em uma alteração das versões anteriores, não há mais suporte para `;` como um separador de literal de matriz.**</span><span class="sxs-lookup"><span data-stu-id="739c8-128">**In a change from earlier versions, `;` is no longer supported as an array literal separator.**</span></span>
- <span data-ttu-id="739c8-129">Os dois-pontos, `:`, são usados para introduzir uma anotação de tipo.</span><span class="sxs-lookup"><span data-stu-id="739c8-129">The colon, `:`, is used to introduce a type annotation.</span></span> <span data-ttu-id="739c8-130">Ele é usado principalmente em assinaturas que podem ser chamadas.</span><span class="sxs-lookup"><span data-stu-id="739c8-130">It is primarily used in callable signatures.</span></span>
  <span data-ttu-id="739c8-131">Como os dois-pontos sempre introduzem uma assinatura de tipo, o operador condicional ternário introduzido no 0.3 usa uma barra vertical, `|`, para separar os valores verdadeiros e falsos; portanto, o Q# usa `cond ? tval | fval` em vez dos dois-pontos como separador, como no C.</span><span class="sxs-lookup"><span data-stu-id="739c8-131">Because colon always introduces a type signature, the ternary conditional operator introduced in 0.3 uses a vertical bar, `|`, to separate the true and false values; thus, Q# uses `cond ? tval | fval` instead of the colon as separator as in C.</span></span>
  
