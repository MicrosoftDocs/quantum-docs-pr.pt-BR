---
title: Configurar o Microsoft QDK (Quantum Development Kit)
description: Aprenda a instalar o Microsoft Quantum Development Kit para diferentes ambientes.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 74b9b3d8f694072f5b5f4d0eb520263387de8919
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834475"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="69c75-103">Configurar o Microsoft QDK (Quantum Development Kit)</span><span class="sxs-lookup"><span data-stu-id="69c75-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="69c75-104">Saiba como configurar o Microsoft QDK (Quantum Development Kit) para seu ambiente e comece a usar a programação quântica.</span><span class="sxs-lookup"><span data-stu-id="69c75-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="69c75-105">O QDK consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="69c75-105">The QDK consists of:</span></span>

- <span data-ttu-id="69c75-106">A linguagem de programação Q#</span><span class="sxs-lookup"><span data-stu-id="69c75-106">The Q# programming language</span></span>
- <span data-ttu-id="69c75-107">Um conjunto de bibliotecas que abstraem o recurso complexo em Q#</span><span class="sxs-lookup"><span data-stu-id="69c75-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="69c75-108">APIs para as linguagens Python e .NET (C#, F# e VB.NET) para executar programas quânticos escritos em Q#</span><span class="sxs-lookup"><span data-stu-id="69c75-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="69c75-109">Ferramentas para facilitar seu desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="69c75-109">Tools to facilitate your development</span></span>

<span data-ttu-id="69c75-110">Os programas Q# podem ser executados como aplicativos autônomos usando o Visual Studio Code ou o Visual Studio, por meio dos Jupyter Notebooks com o kernel lQ# do Jupyter ou emparelhados com um programa host escrito em Python ou em uma linguagem .NET (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="69c75-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="69c75-111">Você também pode executar programas Q# online usando o [Codespaces](https://online.visualstudio.com/), o [MyBinder.org](https://mybinder.org/) ou o [Docker](#use-the-qdk-with-docker).</span><span class="sxs-lookup"><span data-stu-id="69c75-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="69c75-112">Opções para configurar o QDK</span><span class="sxs-lookup"><span data-stu-id="69c75-112">Options for setting up the QDK</span></span>

<span data-ttu-id="69c75-113">Você pode usar o QDK de três maneiras:</span><span class="sxs-lookup"><span data-stu-id="69c75-113">You can use the QDK in three ways:</span></span>

- [<span data-ttu-id="69c75-114">Instalar o QDK localmente</span><span class="sxs-lookup"><span data-stu-id="69c75-114">Install the QDK locally</span></span>](#install-the-qdk-locally)
- [<span data-ttu-id="69c75-115">Usar o QDK online</span><span class="sxs-lookup"><span data-stu-id="69c75-115">Use the QDK online</span></span>](#use-the-qdk-online)
- [<span data-ttu-id="69c75-116">Usar uma imagem do Docker QDK</span><span class="sxs-lookup"><span data-stu-id="69c75-116">Use a QDK Docker image</span></span>](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a><span data-ttu-id="69c75-117">Instalar o QDK localmente</span><span class="sxs-lookup"><span data-stu-id="69c75-117">Install the QDK locally</span></span>

<span data-ttu-id="69c75-118">Você pode desenvolver o código Q# na maioria dos seus IDEs favoritos, bem como integrar Q# a outras linguagens, como Python e .NET (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="69c75-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

|&nbsp; | <span data-ttu-id="69c75-119">**VS Code<br>(2019 ou versões posteriores)**</span><span class="sxs-lookup"><span data-stu-id="69c75-119">**VS Code<br>(2019 or later)**</span></span>| <span data-ttu-id="69c75-120">**Visual Studio<br>(2019 ou versões posteriores)**</span><span class="sxs-lookup"><span data-stu-id="69c75-120">**Visual Studio<br>(2019 or later)**</span></span> | <span data-ttu-id="69c75-121">**Jupyter Notebooks**</span><span class="sxs-lookup"><span data-stu-id="69c75-121">**Jupyter Notebooks**</span></span> | <span data-ttu-id="69c75-122">**Linha de comando**</span><span class="sxs-lookup"><span data-stu-id="69c75-122">**Command line**</span></span>|
|:-----|:-----:|:-----:|:-----:|:-----:|
|<span data-ttu-id="69c75-123">**SO**</span><span class="sxs-lookup"><span data-stu-id="69c75-123">**OS**</span></span> |<span data-ttu-id="69c75-124">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="69c75-124">Windows, macOS, Linux</span></span> |<span data-ttu-id="69c75-125">Somente Windows</span><span class="sxs-lookup"><span data-stu-id="69c75-125">Windows only</span></span> |<span data-ttu-id="69c75-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="69c75-126">Windows, macOS, Linux</span></span> |<span data-ttu-id="69c75-127">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="69c75-127">Windows, macOS, Linux</span></span> |
|<br><span data-ttu-id="69c75-128">**Q# autônomo**</span><span class="sxs-lookup"><span data-stu-id="69c75-128">**Q# standalone**</span></span> |<br>[<span data-ttu-id="69c75-129">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-129">Install</span></span>](xref:microsoft.quantum.install.standalone) |<br> [<span data-ttu-id="69c75-130">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-130">Install</span></span>](xref:microsoft.quantum.install.standalone)  |<br> [<span data-ttu-id="69c75-131">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-131">Install</span></span>](xref:microsoft.quantum.install.jupyter) |<br>[<span data-ttu-id="69c75-132">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-132">Install</span></span>](xref:microsoft.quantum.install.standalone)|
|<span data-ttu-id="69c75-133">**Q# e Python**</span><span class="sxs-lookup"><span data-stu-id="69c75-133">**Q#  and Python**</span></span> |[<span data-ttu-id="69c75-134">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-134">Install</span></span>](xref:microsoft.quantum.install.python) |[<span data-ttu-id="69c75-135">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-135">Install</span></span>](xref:microsoft.quantum.install.python) |[<span data-ttu-id="69c75-136">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-136">Install</span></span>](xref:microsoft.quantum.install.jupyter) |[<span data-ttu-id="69c75-137">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-137">Install</span></span>](xref:microsoft.quantum.install.python) |
|<span data-ttu-id="69c75-138">**Q# e .NET (C#, F#)**</span><span class="sxs-lookup"><span data-stu-id="69c75-138">**Q# and .NET (C#, F#)**</span></span>|[<span data-ttu-id="69c75-139">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-139">Install</span></span>](xref:microsoft.quantum.install.cs) |[<span data-ttu-id="69c75-140">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-140">Install</span></span>](xref:microsoft.quantum.install.cs)|<span data-ttu-id="69c75-141">&#10006;</span><span class="sxs-lookup"><span data-stu-id="69c75-141">&#10006;</span></span> |[<span data-ttu-id="69c75-142">Instalar</span><span class="sxs-lookup"><span data-stu-id="69c75-142">Install</span></span>](xref:microsoft.quantum.install.cs) |

## <a name="use-the-qdk-online"></a><span data-ttu-id="69c75-143">Usar o QDK online</span><span class="sxs-lookup"><span data-stu-id="69c75-143">Use the QDK Online</span></span>

<span data-ttu-id="69c75-144">Você também pode desenvolver o código Q# sem instalar nada localmente com estas opções:</span><span class="sxs-lookup"><span data-stu-id="69c75-144">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="69c75-145">Recurso</span><span class="sxs-lookup"><span data-stu-id="69c75-145">Resource</span></span>|<span data-ttu-id="69c75-146">Vantagens</span><span class="sxs-lookup"><span data-stu-id="69c75-146">Advantages</span></span>|<span data-ttu-id="69c75-147">Limitações</span><span class="sxs-lookup"><span data-stu-id="69c75-147">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="69c75-148">**Codespaces do Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="69c75-148">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="69c75-149">Um ambiente de desenvolvimento online avançado</span><span class="sxs-lookup"><span data-stu-id="69c75-149">A rich online development environment</span></span>  |<span data-ttu-id="69c75-150">Requer uma assinatura e um plano do Azure</span><span class="sxs-lookup"><span data-stu-id="69c75-150">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="69c75-151">**Binder**</span><span class="sxs-lookup"><span data-stu-id="69c75-151">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="69c75-152">Experiência gratuita de notebook online</span><span class="sxs-lookup"><span data-stu-id="69c75-152">Free online notebook experience</span></span> |<span data-ttu-id="69c75-153">Sem persistência</span><span class="sxs-lookup"><span data-stu-id="69c75-153">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="69c75-154">Usar o QDK com o Docker</span><span class="sxs-lookup"><span data-stu-id="69c75-154">Use the QDK with Docker</span></span>

<span data-ttu-id="69c75-155">Você pode usar nossa imagem do Docker QDK em sua instalação local do Docker ou na nuvem por meio de qualquer serviço que dê suporte a imagens do Docker, como a ACI.</span><span class="sxs-lookup"><span data-stu-id="69c75-155">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="69c75-156">Você pode baixar a imagem do Docker IQ# de https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span><span class="sxs-lookup"><span data-stu-id="69c75-156">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="69c75-157">Você também pode usar o Docker com um Contêiner de Desenvolvimento Remoto do Visual Studio Code para definir ambientes de desenvolvimento com rapidez.</span><span class="sxs-lookup"><span data-stu-id="69c75-157">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="69c75-158">Para obter mais informações sobre Contêineres de Desenvolvimento do VS Code, confira https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span><span class="sxs-lookup"><span data-stu-id="69c75-158">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="69c75-159">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="69c75-159">Next steps</span></span>

<span data-ttu-id="69c75-160">Os fluxos de trabalho de cada uma dessas configurações são descritos e comparados em [Maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="69c75-160">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
