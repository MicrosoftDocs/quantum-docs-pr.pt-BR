---
title: Aplicativos de exemplo de química do Quantum
description: Explore aplicativos de exemplo da biblioteca de química do Microsoft Quantum.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples
no-loc:
- Q#
- $$v
ms.openlocfilehash: a0bc79c7fb41069ee7865dbf2f1cfd7851fda32d
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869283"
---
# <a name="quantum-chemistry-examples"></a><span data-ttu-id="e5590-103">Exemplos de química quântica</span><span class="sxs-lookup"><span data-stu-id="e5590-103">Quantum chemistry examples</span></span>

<span data-ttu-id="e5590-104">Nos conceitos de química quântica, criamos manualmente o exemplo de Hamiltonianos fermiônicos.</span><span class="sxs-lookup"><span data-stu-id="e5590-104">In the quantum chemistry concepts, we manually constructed example fermion Hamiltonians.</span></span> <span data-ttu-id="e5590-105">Agora, combinamos os algoritmos de simulação química descritos em [Simulando a Dinâmica Hamiltoniana](xref:microsoft.quantum.libraries.standard.algorithms) com a [estimativa de fase quântica](xref:microsoft.quantum.libraries.characterization) na biblioteca de cânones.</span><span class="sxs-lookup"><span data-stu-id="e5590-105">We now combine the chemistry simulation algorithms outlined in [Simulating Hamiltonian dynamics](xref:microsoft.quantum.libraries.standard.algorithms) with [quantum phase estimation](xref:microsoft.quantum.libraries.characterization) in the canon library.</span></span> <span data-ttu-id="e5590-106">Essa combinação nos permite obter estimativas dos níveis de energia na molécula representada, que é uma das principais aplicações da química quântica em um computador quântico.</span><span class="sxs-lookup"><span data-stu-id="e5590-106">This combination allows us to obtain  estimates of energy levels in the represented molecule, which is one of the key applications of quantum chemistry on a quantum computer.</span></span> 

<span data-ttu-id="e5590-107">Em vez de especificar os termos do Hamiltoniano um por um, também trabalhamos com alguns exemplos que nos permitem executar experimentos de química quântica em escala.</span><span class="sxs-lookup"><span data-stu-id="e5590-107">Instead of specifying terms of the Hamiltonian one-by-one, we also work through some examples that allow us to perform quantum chemistry experiments at scale.</span></span> <span data-ttu-id="e5590-108">Começamos com exemplos que carregam um Hamiltoniano químico codificado no [esquema de Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge).</span><span class="sxs-lookup"><span data-stu-id="e5590-108">We begin with examples that load a chemistry Hamiltonian encoded in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge).</span></span>

<span data-ttu-id="e5590-109">Para moléculas grandes demais para serem simuladas no [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), experimentos científicos interessantes ainda podem ser realizados.</span><span class="sxs-lookup"><span data-stu-id="e5590-109">For molecules that are too large to simulate on the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), interesting science can still be performed.</span></span> <span data-ttu-id="e5590-110">Por exemplo, os custos com recursos para executar simulações químicas grandes ainda podem ser avaliados usando o [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="e5590-110">For instance, the resource costs of performing large chemistry simulations may still be evaluated by targeting the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>

<span data-ttu-id="e5590-111">Agora, vamos ilustrar as aplicações interessantes da biblioteca de simulação química por meio de alguns dos exemplos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="e5590-111">Let us now illustrate interesting applications of the chemistry simulation library through a few of the provided samples.</span></span>
