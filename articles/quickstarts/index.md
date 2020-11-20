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
ms.openlocfilehash: f0c3df1998f9b64ff6544867b83a7afe52b6f46d
ms.sourcegitcommit: fd57a845d013ae4578715d04b1ed1edc1c8ff6b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "94870750"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="66b80-103">Configurar o Microsoft QDK (Quantum Development Kit)</span><span class="sxs-lookup"><span data-stu-id="66b80-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="66b80-104">Saiba como configurar o Microsoft QDK (Quantum Development Kit) para seu ambiente e comece a usar a programação quântica.</span><span class="sxs-lookup"><span data-stu-id="66b80-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="66b80-105">O QDK consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="66b80-105">The QDK consists of:</span></span>

- <span data-ttu-id="66b80-106">A linguagem de programação Q#</span><span class="sxs-lookup"><span data-stu-id="66b80-106">The Q# programming language</span></span>
- <span data-ttu-id="66b80-107">Um conjunto de bibliotecas que abstraem o recurso complexo em Q#</span><span class="sxs-lookup"><span data-stu-id="66b80-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="66b80-108">APIs para as linguagens Python e .NET (C#, F# e VB.NET) para executar programas quânticos escritos em Q#</span><span class="sxs-lookup"><span data-stu-id="66b80-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="66b80-109">Ferramentas para facilitar seu desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="66b80-109">Tools to facilitate your development</span></span>

<span data-ttu-id="66b80-110">Os programas Q# podem ser executados como aplicativos autônomos usando o Visual Studio Code ou o Visual Studio, por meio dos Jupyter Notebooks com o kernel lQ# do Jupyter ou emparelhados com um programa host escrito em Python ou em uma linguagem .NET (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="66b80-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="66b80-111">Você também pode executar programas Q# online usando o [Codespaces](https://online.visualstudio.com/), o [MyBinder.org](https://mybinder.org/) ou o [Docker](#use-the-qdk-with-docker).</span><span class="sxs-lookup"><span data-stu-id="66b80-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="66b80-112">Opções para configurar o QDK</span><span class="sxs-lookup"><span data-stu-id="66b80-112">Options for setting up the QDK</span></span>

<span data-ttu-id="66b80-113">Você pode usar o QDK de três maneiras:</span><span class="sxs-lookup"><span data-stu-id="66b80-113">You can use the QDK in three ways:</span></span>

- [<span data-ttu-id="66b80-114">Instalar o QDK localmente</span><span class="sxs-lookup"><span data-stu-id="66b80-114">Install the QDK locally</span></span>](#install-the-qdk-locally)
- [<span data-ttu-id="66b80-115">Usar o QDK online</span><span class="sxs-lookup"><span data-stu-id="66b80-115">Use the QDK online</span></span>](#use-the-qdk-online)
- [<span data-ttu-id="66b80-116">Usar uma imagem do Docker QDK</span><span class="sxs-lookup"><span data-stu-id="66b80-116">Use a QDK Docker image</span></span>](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a><span data-ttu-id="66b80-117">Instalar o QDK localmente</span><span class="sxs-lookup"><span data-stu-id="66b80-117">Install the QDK locally</span></span>

<span data-ttu-id="66b80-118">Você pode desenvolver o código Q# na maioria dos seus IDEs favoritos, bem como integrar Q# a outras linguagens, como Python e .NET (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="66b80-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><span data-ttu-id="66b80-119"><b>Código VS</span><span class="sxs-lookup"><span data-stu-id="66b80-119"><b>VS Code</span></span><br><span data-ttu-id="66b80-120">(2019 ou posterior)</b></span><span class="sxs-lookup"><span data-stu-id="66b80-120">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="VS Studio" width="50"/><br><span data-ttu-id="66b80-121"><b>VS Studio</span><span class="sxs-lookup"><span data-stu-id="66b80-121"><b>VS Studio</span></span><br><span data-ttu-id="66b80-122">(2019 ou posterior)</b></span><span class="sxs-lookup"><span data-stu-id="66b80-122">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><span data-ttu-id="66b80-123"><b>Jupyter Notebooks</b></span><span class="sxs-lookup"><span data-stu-id="66b80-123"><b>Jupyter Notebooks</b></span></span></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><span data-ttu-id="66b80-124"><b>Linha de comando</b></span><span class="sxs-lookup"><span data-stu-id="66b80-124"><b>Command line</b></span></span></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><span data-ttu-id="66b80-125"><b>Suporte a SO:</b></span><span class="sxs-lookup"><span data-stu-id="66b80-125"><b>OS support:</b></span></span></td>
        <td align="center"><span data-ttu-id="66b80-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="66b80-126">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="66b80-127">Somente Windows</span><span class="sxs-lookup"><span data-stu-id="66b80-127">Windows only</span></span></td>
        <td align="center"><span data-ttu-id="66b80-128">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="66b80-128">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="66b80-129">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="66b80-129">Windows, macOS, Linux</span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><span data-ttu-id="66b80-130"><b>Q# autônomo</b></span><span class="sxs-lookup"><span data-stu-id="66b80-130"><b>Q# standalone</b></span></span></td>
        <td align="center"><span data-ttu-id="66b80-131"><a href="xref:microsoft.quantum.install.standalone">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-131"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="66b80-132"><a href="xref:microsoft.quantum.install.standalone">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-132"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="66b80-133"><a href="xref:microsoft.quantum.install.jupyter">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-133"><a href="xref:microsoft.quantum.install.jupyter">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="66b80-134"><a href="xref:microsoft.quantum.install.standalone">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-134"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><span data-ttu-id="66b80-135"><b>Q# e Python</b></span><span class="sxs-lookup"><span data-stu-id="66b80-135"><b>Q# and Python</b></span></span></td>
        <td align="center"><span data-ttu-id="66b80-136"><a href="xref:microsoft.quantum.install.python">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-136"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="66b80-137"><a href="xref:microsoft.quantum.install.python">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-137"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="66b80-138"><a href="xref:microsoft.quantum.install.jupyter">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-138"><a href="xref:microsoft.quantum.install.jupyter">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="66b80-139"><a href="xref:microsoft.quantum.install.python">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-139"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><span data-ttu-id="66b80-140"><b>Q# e .NET (C#, F#)</b></span><span class="sxs-lookup"><span data-stu-id="66b80-140"><b>Q# and .NET (C#, F#)</b></span></span></td> 
        <td align="center"><span data-ttu-id="66b80-141"><a href="xref:microsoft.quantum.install.cs">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-141"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="66b80-142"><a href="xref:microsoft.quantum.install.cs">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-142"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="66b80-143">&#10006;</span><span class="sxs-lookup"><span data-stu-id="66b80-143">&#10006;</span></span></td>
        <td align="center"><span data-ttu-id="66b80-144"><a href="xref:microsoft.quantum.install.cs">Instalar</a></span><span class="sxs-lookup"><span data-stu-id="66b80-144"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
   </tr>
</table>

## <a name="use-the-qdk-online"></a><span data-ttu-id="66b80-145">Usar o QDK online</span><span class="sxs-lookup"><span data-stu-id="66b80-145">Use the QDK Online</span></span>

<span data-ttu-id="66b80-146">Você também pode desenvolver o código Q# sem instalar nada localmente com estas opções:</span><span class="sxs-lookup"><span data-stu-id="66b80-146">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="66b80-147">Recurso</span><span class="sxs-lookup"><span data-stu-id="66b80-147">Resource</span></span>|<span data-ttu-id="66b80-148">Vantagens</span><span class="sxs-lookup"><span data-stu-id="66b80-148">Advantages</span></span>|<span data-ttu-id="66b80-149">Limitações</span><span class="sxs-lookup"><span data-stu-id="66b80-149">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="66b80-150">**Codespaces do Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="66b80-150">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="66b80-151">Um ambiente de desenvolvimento online avançado</span><span class="sxs-lookup"><span data-stu-id="66b80-151">A rich online development environment</span></span>  |<span data-ttu-id="66b80-152">Requer uma assinatura e um plano do Azure</span><span class="sxs-lookup"><span data-stu-id="66b80-152">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="66b80-153">**Binder**</span><span class="sxs-lookup"><span data-stu-id="66b80-153">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="66b80-154">Experiência gratuita de notebook online</span><span class="sxs-lookup"><span data-stu-id="66b80-154">Free online notebook experience</span></span> |<span data-ttu-id="66b80-155">Sem persistência</span><span class="sxs-lookup"><span data-stu-id="66b80-155">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="66b80-156">Usar o QDK com o Docker</span><span class="sxs-lookup"><span data-stu-id="66b80-156">Use the QDK with Docker</span></span>

<span data-ttu-id="66b80-157">Você pode usar nossa imagem do Docker QDK em sua instalação local do Docker ou na nuvem por meio de qualquer serviço que dê suporte a imagens do Docker, como a ACI.</span><span class="sxs-lookup"><span data-stu-id="66b80-157">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="66b80-158">Você pode baixar a imagem do Docker IQ# de https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span><span class="sxs-lookup"><span data-stu-id="66b80-158">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="66b80-159">Você também pode usar o Docker com um Contêiner de Desenvolvimento Remoto do Visual Studio Code para definir ambientes de desenvolvimento com rapidez.</span><span class="sxs-lookup"><span data-stu-id="66b80-159">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="66b80-160">Para obter mais informações sobre Contêineres de Desenvolvimento do VS Code, confira https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span><span class="sxs-lookup"><span data-stu-id="66b80-160">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="66b80-161">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="66b80-161">Next steps</span></span>

<span data-ttu-id="66b80-162">Os fluxos de trabalho de cada uma dessas configurações são descritos e comparados em [Maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="66b80-162">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
