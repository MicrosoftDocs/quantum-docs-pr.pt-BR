---
title: 'Desenvolver com aplicativos de linha de comando Q #'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630269"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="e3cae-102">Desenvolver com aplicativos de linha de comando Q #</span><span class="sxs-lookup"><span data-stu-id="e3cae-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="e3cae-103">Os programas da Q # podem ser executados por conta própria, sem um driver em uma linguagem de host como C#, F # ou Python.</span><span class="sxs-lookup"><span data-stu-id="e3cae-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e3cae-104">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e3cae-104">Prerequisites</span></span>

- [<span data-ttu-id="e3cae-105">SDK do .NET Core 3,1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e3cae-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="e3cae-106">Instalação</span><span class="sxs-lookup"><span data-stu-id="e3cae-106">Installation</span></span>

<span data-ttu-id="e3cae-107">Embora você possa criar aplicativos de linha de comando Q # em qualquer IDE, é recomendável usar Visual Studio Code (VS Code) ou IDE do Visual Studio para seus aplicativos do Q #.</span><span class="sxs-lookup"><span data-stu-id="e3cae-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="e3cae-108">O desenvolvimento nessas ferramentas fornece acesso a funcionalidades avançadas.</span><span class="sxs-lookup"><span data-stu-id="e3cae-108">Developing in these tools provides access to rich functionality.</span></span>

<span data-ttu-id="e3cae-109">Para configurar VS Code:</span><span class="sxs-lookup"><span data-stu-id="e3cae-109">To configure VS Code:</span></span>

1. <span data-ttu-id="e3cae-110">Baixe e instale o [vs Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).</span><span class="sxs-lookup"><span data-stu-id="e3cae-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="e3cae-111">Instale o [Microsoft QDK para vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="e3cae-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="e3cae-112">Para configurar o Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="e3cae-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="e3cae-113">Baixe e instale o [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16,3 ou superior, com a carga de trabalho de desenvolvimento de plataforma cruzada do .NET Core habilitada.</span><span class="sxs-lookup"><span data-stu-id="e3cae-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="e3cae-114">Baixe e instale o [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="e3cae-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="e3cae-115">Desenvolver com Q # usando VS Code</span><span class="sxs-lookup"><span data-stu-id="e3cae-115">Develop with Q# using VS Code</span></span>

<span data-ttu-id="e3cae-116">Instale os modelos de projeto do Q #:</span><span class="sxs-lookup"><span data-stu-id="e3cae-116">Install the Q# project templates:</span></span>

1. <span data-ttu-id="e3cae-117">Abra o VS Code.</span><span class="sxs-lookup"><span data-stu-id="e3cae-117">Open VS Code.</span></span>
2. <span data-ttu-id="e3cae-118">Clique em **Exibir**  ->  **paleta de comandos**.</span><span class="sxs-lookup"><span data-stu-id="e3cae-118">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="e3cae-119">Selecione **Q #: instalar modelos de projeto**.</span><span class="sxs-lookup"><span data-stu-id="e3cae-119">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="e3cae-120">Quando os **modelos de projeto forem instalados com êxito** , o QDK estará pronto para uso com seus próprios aplicativos e bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="e3cae-120">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="e3cae-121">Para criar um novo projeto:</span><span class="sxs-lookup"><span data-stu-id="e3cae-121">To create a new project:</span></span>

1. <span data-ttu-id="e3cae-122">Clique em **Exibir**  ->  **paleta de comandos** e selecione **Q #: criar novo projeto**.</span><span class="sxs-lookup"><span data-stu-id="e3cae-122">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="e3cae-123">Clique em **aplicativo de console autônomo**.</span><span class="sxs-lookup"><span data-stu-id="e3cae-123">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="e3cae-124">Navegue até o local para salvar o projeto e clique em **criar projeto**.</span><span class="sxs-lookup"><span data-stu-id="e3cae-124">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="e3cae-125">Quando o projeto for criado com êxito, clique em **abrir novo projeto...** no canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="e3cae-125">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="e3cae-126">Inspecione o projeto.</span><span class="sxs-lookup"><span data-stu-id="e3cae-126">Inspect the project.</span></span> <span data-ttu-id="e3cae-127">Você deve ver um arquivo de origem chamado `Program.qs` , que é um programa Q # que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="e3cae-127">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="e3cae-128">Para executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="e3cae-128">To run the application:</span></span>
1. <span data-ttu-id="e3cae-129">Clique em **terminal**  ->  **novo terminal**.</span><span class="sxs-lookup"><span data-stu-id="e3cae-129">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="e3cae-130">No prompt do terminal, digite `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="e3cae-130">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="e3cae-131">Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="e3cae-131">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="e3cae-132">Os espaços de trabalho com várias pastas raiz não têm suporte atualmente pela extensão VS Code Q #.</span><span class="sxs-lookup"><span data-stu-id="e3cae-132">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="e3cae-133">Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="e3cae-133">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="e3cae-134">Desenvolver com Q # usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3cae-134">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="e3cae-135">Verifique sua instalação do Visual Studio criando um aplicativo Q # `Hello World` .</span><span class="sxs-lookup"><span data-stu-id="e3cae-135">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="e3cae-136">Para criar um novo aplicativo Q #:</span><span class="sxs-lookup"><span data-stu-id="e3cae-136">To create a new Q# application:</span></span>
1. <span data-ttu-id="e3cae-137">Abra o Visual Studio e clique em **arquivo**  ->  **novo**  ->  **projeto**.</span><span class="sxs-lookup"><span data-stu-id="e3cae-137">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="e3cae-138">Digite `Q#` na caixa de pesquisa, selecione **aplicativo Q #** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e3cae-138">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="e3cae-139">Insira um nome e um local para seu aplicativo e clique em **criar**.</span><span class="sxs-lookup"><span data-stu-id="e3cae-139">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="e3cae-140">Inspecione o projeto.</span><span class="sxs-lookup"><span data-stu-id="e3cae-140">Inspect the project.</span></span> <span data-ttu-id="e3cae-141">Você deve ver um arquivo de origem chamado `Program.qs` , que é um programa Q # que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="e3cae-141">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="e3cae-142">Para executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="e3cae-142">To run the application:</span></span>
1. <span data-ttu-id="e3cae-143">Selecione **depurar**  ->  **Iniciar sem depuração**.</span><span class="sxs-lookup"><span data-stu-id="e3cae-143">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="e3cae-144">Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.</span><span class="sxs-lookup"><span data-stu-id="e3cae-144">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="e3cae-145">Se você tiver vários projetos dentro de uma solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta que a solução, ou em uma de suas subpastas.</span><span class="sxs-lookup"><span data-stu-id="e3cae-145">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  


## <a name="next-steps"></a><span data-ttu-id="e3cae-146">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="e3cae-146">Next steps</span></span>

<span data-ttu-id="e3cae-147">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="e3cae-147">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
