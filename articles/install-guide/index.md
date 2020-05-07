---
title: Saiba como instalar o QDK (Microsoft Quantum development kit)
description: Como instalar o Microsoft Quantum Development Kit para ambientes de C#, Python e Jupyter Notebook.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: bca700660094b91f1c0dfa03f9bce1336073ca51
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680185"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="c46f2-103">Instalar o QDK (Microsoft Quantum development kit)</span><span class="sxs-lookup"><span data-stu-id="c46f2-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="c46f2-104">Saiba como instalar o QDK (Microsoft Quantum development kit) para começar a usar a programação quântica.</span><span class="sxs-lookup"><span data-stu-id="c46f2-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="c46f2-105">O QDK consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="c46f2-105">The QDK consists of:</span></span>

- <span data-ttu-id="c46f2-106">a linguagem de programação Q#</span><span class="sxs-lookup"><span data-stu-id="c46f2-106">the Q# programming language</span></span>
- <span data-ttu-id="c46f2-107">um conjunto de bibliotecas que abstrai a funcionalidade complexa no Q#</span><span class="sxs-lookup"><span data-stu-id="c46f2-107">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="c46f2-108">APIs para as linguagens Python e .Net (C#, F# e VB.NET) para executar programas quânticos escritos em Q#</span><span class="sxs-lookup"><span data-stu-id="c46f2-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="c46f2-109">ferramentas para facilitar seu desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="c46f2-109">tools to facilitate your development</span></span>

<span data-ttu-id="c46f2-110">Os programas em Q# geralmente são emparelhados com um programa de host escrito em uma linguagem de programação do .NET (normalmente C#) ou no Python.</span><span class="sxs-lookup"><span data-stu-id="c46f2-110">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="c46f2-111">Isso nos permite chamar operações quânticas de dentro de um programa clássico.</span><span class="sxs-lookup"><span data-stu-id="c46f2-111">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="c46f2-112">Além disso, o QDK fornece suporte a Q# para Jupyter Notebooks com o kernel IQ# do Jupyter.</span><span class="sxs-lookup"><span data-stu-id="c46f2-112">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="c46f2-113">O QDK está disponível para vários ambientes de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="c46f2-113">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="c46f2-114">Selecione sua configuração preferida nas seções abaixo:</span><span class="sxs-lookup"><span data-stu-id="c46f2-114">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="c46f2-115">[Aplicativo de linha de comando do Q#:](xref:microsoft.quantum.install.standalone) escolha essa abordagem se quiser trabalhar com o Q# na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c46f2-115">[Q# command line application:](xref:microsoft.quantum.install.standalone) choose this approach if you want to work with Q# from the command line.</span></span> <span data-ttu-id="c46f2-116">Isso não exige um driver ou um programa de host como as opções abaixo.</span><span class="sxs-lookup"><span data-stu-id="c46f2-116">This does not require a driver or a host program like the below options.</span></span>
- <span data-ttu-id="c46f2-117">[Instalar o Q # para Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) escolha esse ambiente para executar o código de Q # em células com texto inserido ou criar tutoriais interativos de computação quântica.</span><span class="sxs-lookup"><span data-stu-id="c46f2-117">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 
- <span data-ttu-id="c46f2-118">[Desenvolver com o Q# e Python:](xref:microsoft.quantum.install.python) se você desejar combinar o Python e o Q# para criar um programa de host do Python que chame operações do Q#.</span><span class="sxs-lookup"><span data-stu-id="c46f2-118">[Develop with Q# and Python:](xref:microsoft.quantum.install.python) if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="c46f2-119">[Desenvolver com o C# ou F#:](xref:microsoft.quantum.install.cs) se você desejar combinar o C# ou o F# para criar um programa de host do .NET que chame operações do Q#.</span><span class="sxs-lookup"><span data-stu-id="c46f2-119">[Develop with Q# and C# or F#:](xref:microsoft.quantum.install.cs) if you want to combine C# or F# and Q# to create a .NET host program that calls Q# operations.</span></span>
