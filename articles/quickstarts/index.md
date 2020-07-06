---
title: Instalar o QDK (Microsoft Quantum development kit)
description: Como instalar o Microsoft Quantum Development Kit para diferentes ambientes.
author: bradben
ms.author: bradben
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: ee8d210d67a20cfea3bdc36162efc47f021a6dc6
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885459"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="acb34-103">Instalar o QDK (Microsoft Quantum development kit)</span><span class="sxs-lookup"><span data-stu-id="acb34-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="acb34-104">Saiba como instalar o QDK (Microsoft Quantum development kit) para começar a usar a programação quântica.</span><span class="sxs-lookup"><span data-stu-id="acb34-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="acb34-105">O QDK consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="acb34-105">The QDK consists of:</span></span>

- <span data-ttu-id="acb34-106">A linguagem de programação Q#</span><span class="sxs-lookup"><span data-stu-id="acb34-106">The Q# programming language</span></span>
- <span data-ttu-id="acb34-107">Um conjunto de bibliotecas que abstraem a funcionalidade complexa em Q#</span><span class="sxs-lookup"><span data-stu-id="acb34-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="acb34-108">APIs para as linguagens Python e .Net (C#, F# e VB.NET) para executar programas quânticos escritos em Q#</span><span class="sxs-lookup"><span data-stu-id="acb34-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="acb34-109">Ferramentas para facilitar seu desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="acb34-109">Tools to facilitate your development</span></span>

<span data-ttu-id="acb34-110">Os programas Q# podem ser executados como aplicativos autônomos usando o Visual Studio Code ou o Visual Studio ou por meio de Jupyter Notebooks com o kernel IQ# do Jupyter.</span><span class="sxs-lookup"><span data-stu-id="acb34-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, or through Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>
<span data-ttu-id="acb34-111">Eles também podem ser emparelhados com um programa host escrito em uma linguagem .NET (normalmente C# ) ou Python, permitindo que você chame operações quantum de dentro de um programa clássico.</span><span class="sxs-lookup"><span data-stu-id="acb34-111">They can also be paired with a host program written in a .NET language (typically C#) or Python, enabling you to call quantum operations from inside a classical program.</span></span>

<span data-ttu-id="acb34-112">Os fluxos de trabalho de cada uma dessas configurações são descritos e comparados em [Maneiras de executar um programa em Q#](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="acb34-112">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

<span data-ttu-id="acb34-113">Para prosseguir com a instalação do QDK e com a criação de projetos em Q#, selecione a configuração de sua preferência:</span><span class="sxs-lookup"><span data-stu-id="acb34-113">To proceed with installing the QDK and creating Q# projects, select your preferred setup:</span></span>

<span data-ttu-id="acb34-114">[Desenvolver com aplicativos de linha de comando do Q#](xref:microsoft.quantum.install.standalone) – Escolha essa abordagem para trabalhar com o Q# na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="acb34-114">[Develop with Q# command line applications](xref:microsoft.quantum.install.standalone) - Choose this approach to work with Q# from the command line.</span></span> <span data-ttu-id="acb34-115">Isso não exige um driver ou um programa de host como as opções abaixo.</span><span class="sxs-lookup"><span data-stu-id="acb34-115">This does not require a driver or a host program like the below options.</span></span>

<span data-ttu-id="acb34-116">[Desenvolver com Jupyter Notebooks em Q#](xref:microsoft.quantum.install.jupyter) – Selecione esse ambiente para executar o código do Q# em células com texto inserido ou criar tutoriais interativos de computação quântica.</span><span class="sxs-lookup"><span data-stu-id="acb34-116">[Develop with Q# Jupyter Notebooks](xref:microsoft.quantum.install.jupyter) - Select this environment to run Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 

<span data-ttu-id="acb34-117">[Desenvolver com Q# e Python](xref:microsoft.quantum.install.python) – Permite que você combine o Python e o Q# para criar um programa do host do Python que chama operações Q#.</span><span class="sxs-lookup"><span data-stu-id="acb34-117">[Develop with Q# and Python](xref:microsoft.quantum.install.python) - Enables you to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>

<span data-ttu-id="acb34-118">[Desenvolver com Q# e .NET](xref:microsoft.quantum.install.cs) – Combine C#, F# e VB.NET com Q# para criar um programa do host do .NET que chama operações Q#.</span><span class="sxs-lookup"><span data-stu-id="acb34-118">[Develop with Q# and .NET](xref:microsoft.quantum.install.cs) - Combine C#, F#, or VB.NET with Q# to create a .NET host program that calls Q# operations.</span></span>
