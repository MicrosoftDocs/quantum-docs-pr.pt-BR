---
title: Instalar o QDK (Microsoft Quantum development kit)
description: Como instalar o Microsoft Quantum Development Kit para diferentes ambientes.
author: natke
ms.author: nakersha
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: a5230f506bce02c331d22d6a428b3bd92052bbd4
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327553"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="1d803-103">Instalar o QDK (Microsoft Quantum development kit)</span><span class="sxs-lookup"><span data-stu-id="1d803-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="1d803-104">Saiba como instalar o QDK (Microsoft Quantum development kit) para começar a usar a programação quântica.</span><span class="sxs-lookup"><span data-stu-id="1d803-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="1d803-105">O QDK consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="1d803-105">The QDK consists of:</span></span>

- <span data-ttu-id="1d803-106">A linguagem de programação Q#</span><span class="sxs-lookup"><span data-stu-id="1d803-106">The Q# programming language</span></span>
- <span data-ttu-id="1d803-107">Um conjunto de bibliotecas que abstraem a funcionalidade complexa em Q#</span><span class="sxs-lookup"><span data-stu-id="1d803-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="1d803-108">APIs para as linguagens Python e .Net (C#, F# e VB.NET) para executar programas quânticos escritos em Q#</span><span class="sxs-lookup"><span data-stu-id="1d803-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="1d803-109">Ferramentas para facilitar seu desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="1d803-109">Tools to facilitate your development</span></span>

<span data-ttu-id="1d803-110">Os programas Q# podem ser executados como aplicativos autônomos usando o Visual Studio Code ou o Visual Studio ou por meio de Jupyter Notebooks com o kernel IQ# do Jupyter.</span><span class="sxs-lookup"><span data-stu-id="1d803-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, or through Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="1d803-111">Eles também podem ser emparelhados com um programa host escrito em uma linguagem .NET (normalmente C# ) ou Python, permitindo que você chame operações quantum de dentro de um programa clássico.</span><span class="sxs-lookup"><span data-stu-id="1d803-111">They can also be paired with a host program written in a .NET language (typically C#) or Python, enabling you to call quantum operations from inside a classical program.</span></span>

<span data-ttu-id="1d803-112">O QDK está disponível para vários ambientes de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="1d803-112">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="1d803-113">Selecione a configuração preferencial entre:</span><span class="sxs-lookup"><span data-stu-id="1d803-113">Select your preferred setup from:</span></span>

<span data-ttu-id="1d803-114">[Desenvolver com aplicativos de linha de comando do Q#](xref:microsoft.quantum.install.standalone) – Escolha essa abordagem para trabalhar com o Q# na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1d803-114">[Develop with Q# command line applications](xref:microsoft.quantum.install.standalone) - Choose this approach to work with Q# from the command line.</span></span> <span data-ttu-id="1d803-115">Isso não exige um driver ou um programa de host como as opções abaixo.</span><span class="sxs-lookup"><span data-stu-id="1d803-115">This does not require a driver or a host program like the below options.</span></span>

<span data-ttu-id="1d803-116">[Desenvolver com Jupyter Notebooks em Q#](xref:microsoft.quantum.install.jupyter) – Selecione esse ambiente para executar o código do Q# em células com texto inserido ou criar tutoriais interativos de computação quântica.</span><span class="sxs-lookup"><span data-stu-id="1d803-116">[Develop with Q# Jupyter Notebooks](xref:microsoft.quantum.install.jupyter) - Select this environment to run Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 

<span data-ttu-id="1d803-117">[Desenvolver com Q# e Python](xref:microsoft.quantum.install.python) – Permite que você combine o Python e o Q# para criar um programa do host do Python que chama operações Q#.</span><span class="sxs-lookup"><span data-stu-id="1d803-117">[Develop with Q# and Python](xref:microsoft.quantum.install.python) - Enables you to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>

<span data-ttu-id="1d803-118">[Desenvolver com Q# e .NET](xref:microsoft.quantum.install.cs) – Combine C#, F# e VB.NET com Q# para criar um programa do host do .NET que chama operações Q#.</span><span class="sxs-lookup"><span data-stu-id="1d803-118">[Develop with Q# and .NET](xref:microsoft.quantum.install.cs) - Combine C#, F#, or VB.NET with Q# to create a .NET host program that calls Q# operations.</span></span>
