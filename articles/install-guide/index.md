---
title: Saiba como instalar o QDK (Microsoft Quantum development kit)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 0e9dd1c74316eeb1fa7bbbf657d2e78231ee4294
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036501"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="7241a-102">Instalar o QDK (Microsoft Quantum development kit)</span><span class="sxs-lookup"><span data-stu-id="7241a-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="7241a-103">Saiba como instalar o QDK (Microsoft Quantum development kit) para começar a usar a programação quântica.</span><span class="sxs-lookup"><span data-stu-id="7241a-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="7241a-104">O QDK consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="7241a-104">The QDK consists of:</span></span>

- <span data-ttu-id="7241a-105">a linguagem de programação Q#</span><span class="sxs-lookup"><span data-stu-id="7241a-105">the Q# programming language</span></span>
- <span data-ttu-id="7241a-106">um conjunto de bibliotecas que abstrai a funcionalidade complexa no Q#</span><span class="sxs-lookup"><span data-stu-id="7241a-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="7241a-107">APIs para as linguagens Python e .Net (C#, F# e VB.NET) para executar programas quânticos escritos em Q#</span><span class="sxs-lookup"><span data-stu-id="7241a-107">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="7241a-108">ferramentas para facilitar seu desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="7241a-108">tools to facilitate your development</span></span>

<span data-ttu-id="7241a-109">Os programas em Q# geralmente são emparelhados com um programa de host escrito em uma linguagem de programação do .NET (normalmente C#) ou no Python.</span><span class="sxs-lookup"><span data-stu-id="7241a-109">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="7241a-110">Isso nos permite chamar operações quânticas de dentro de um programa clássico.</span><span class="sxs-lookup"><span data-stu-id="7241a-110">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="7241a-111">Além disso, o QDK fornece suporte a Q# para Jupyter Notebooks com o kernel IQ# do Jupyter.</span><span class="sxs-lookup"><span data-stu-id="7241a-111">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="7241a-112">O QDK está disponível para vários ambientes de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="7241a-112">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="7241a-113">Selecione sua configuração preferida nas seções abaixo:</span><span class="sxs-lookup"><span data-stu-id="7241a-113">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="7241a-114">[Instalar o Q# para C#:](xref:microsoft.quantum.install.cs) escolha esse ambiente se você desejar combinar C# e Q# para criar um programa de host do C# que chame operações do Q#.</span><span class="sxs-lookup"><span data-stu-id="7241a-114">[Install Q# for C#:](xref:microsoft.quantum.install.cs) choose this environment if you want to combine C# and Q# to create a C# host program that calls Q# operations.</span></span>
- <span data-ttu-id="7241a-115">[Instalar o Q# para Python:](xref:microsoft.quantum.install.python) escolha esse ambiente se você desejar combinar Python e Q# para criar um programa de host do Python que chame operações do Q#.</span><span class="sxs-lookup"><span data-stu-id="7241a-115">[Install Q# for Python:](xref:microsoft.quantum.install.python) choose this environment if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="7241a-116">[Instalar o Q # para Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) escolha esse ambiente para executar o código de Q # em células com texto inserido ou criar tutoriais interativos de computação quântica.</span><span class="sxs-lookup"><span data-stu-id="7241a-116">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> <span data-ttu-id="7241a-117">Não escolha esse ambiente se desejar combinar o Q# com um programa de host clássico externo.</span><span class="sxs-lookup"><span data-stu-id="7241a-117">Do not choose this environment if you want to combine Q# with an external classical host program.</span></span>
