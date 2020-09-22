---
title: Bibliotecas do Quantum Development Kit
description: Visão geral das bibliotecas padrão, de química e de valores numéricos incluídas no Microsoft Quantum Development Kit.
author: cgranade
ms.author: chgranad
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries
no-loc:
- Q#
- $$v
ms.openlocfilehash: 90672b6ec78bf8305bdb3ab8326002cf8ce34bfe
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835716"
---
# <a name="overview-of-no-locq-libraries"></a><span data-ttu-id="811bb-103">Visão geral das bibliotecas de Q#</span><span class="sxs-lookup"><span data-stu-id="811bb-103">Overview of Q# Libraries</span></span>
<span data-ttu-id="811bb-104">O Quantum Development Kit é fornecido com várias bibliotecas para facilitar o desenvolvimento de aplicativos quânticos em Q#.</span><span class="sxs-lookup"><span data-stu-id="811bb-104">The Quantum Development Kit is provided with several libraries to make it easier to develop quantum applications in Q#.</span></span>
<span data-ttu-id="811bb-105">Nesta seção da documentação, descrevemos essas bibliotecas e como usá-las em seus programas.</span><span class="sxs-lookup"><span data-stu-id="811bb-105">In this section of the documentation, we describe these libraries and how to use them in your programs.</span></span>

- <span data-ttu-id="811bb-106">[**Bibliotecas padrão**](xref:microsoft.quantum.libraries.standard.intro): Esta seção descreve o prelúdio, que define a interface entre programas Q# e os computadores de destino, e o cânone, uma biblioteca de Q# que fornece operações e funções de uso geral para escrever programas Q#.</span><span class="sxs-lookup"><span data-stu-id="811bb-106">[**Standard libraries**](xref:microsoft.quantum.libraries.standard.intro): This section describes the prelude, which defines the interface between Q# programs and target machines, and the canon, a Q# library that provides general-purpose operations and functions for use in writing Q# programs.</span></span>
- <span data-ttu-id="811bb-107">[**Biblioteca de química quântica**](xref:microsoft.quantum.chemistry.concepts.intro): esta seção descreve a biblioteca química quântica, que fornece um modelo de dados para carregar representações de operações de simulação quântica e de Hamiltonianos fermiônicos, bem como funções que atuam nessas representações.</span><span class="sxs-lookup"><span data-stu-id="811bb-107">[**Quantum chemistry library**](xref:microsoft.quantum.chemistry.concepts.intro): This section describes the quantum chemistry library, which provides a data model for loading representations of fermionic Hamiltonians and quantum simulation operations and functions which act on these representations.</span></span>
- <span data-ttu-id="811bb-108">[**Biblioteca de numéricos quânticos**](xref:microsoft.quantum.numerics.intro): esta seção descreve a biblioteca de numéricos quânticos, que fornece implementações para uma gama de funções matemáticas.</span><span class="sxs-lookup"><span data-stu-id="811bb-108">[**Quantum numerics library**](xref:microsoft.quantum.numerics.intro): This section describes the quantum numerics library, which provides implementations for a host of mathematical functions.</span></span> <span data-ttu-id="811bb-109">Ela dá suporte a representações de ponto fixo e inteiro (com e sem sinal).</span><span class="sxs-lookup"><span data-stu-id="811bb-109">It supports integer (signed & unsigned) and fixed-point representations.</span></span>
- <span data-ttu-id="811bb-110">[**Biblioteca de machine learning quântica**](xref:microsoft.quantum.machine-learning.concepts.intro): Esta seção descreve a biblioteca de machine learning quântica, que fornece uma implementação dos classificadores sequenciais que aproveitam a computação quântica para entender os dados.</span><span class="sxs-lookup"><span data-stu-id="811bb-110">[**Quantum machine learning library**](xref:microsoft.quantum.machine-learning.concepts.intro): This section describes the quantum machine learning library, which provides an implementation of the sequential classifiers that take advantage of quantum computing to understand data.</span></span>

<span data-ttu-id="811bb-111">As fontes das bibliotecas, bem como exemplos de código, podem ser obtidos no GitHub.</span><span class="sxs-lookup"><span data-stu-id="811bb-111">Sources of the libraries as well as code samples can be obtained from GitHub.</span></span>
<span data-ttu-id="811bb-112">Confira [Licenciamento](xref:microsoft.quantum.libraries.licensing) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="811bb-112">See [Licensing](xref:microsoft.quantum.libraries.licensing) for further information.</span></span> <span data-ttu-id="811bb-113">Observe que as referências do pacote ("binários") também estão disponíveis para as bibliotecas e fornecem outra maneira de incluir as bibliotecas em projetos.</span><span class="sxs-lookup"><span data-stu-id="811bb-113">Note that package references ("binaries") are available also for the libraries and offer another way of including the libraries in projects.</span></span>
<span data-ttu-id="811bb-114">Um modo conveniente de obtê-las é por meio do [NuGet](https://nuget.org).</span><span class="sxs-lookup"><span data-stu-id="811bb-114">A convenient way of obtaining them is via [NuGet](https://nuget.org).</span></span>
