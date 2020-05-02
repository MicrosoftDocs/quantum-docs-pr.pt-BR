---
title: 'Executar programas de Q # sem um driver e um idioma de host'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e83acaf10af952da06abf4737ad2ec91f1cf1b8e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82706794"
---
# <a name="q-command-line-applications"></a><span data-ttu-id="2d525-102">Q # aplicativos de linha de comando</span><span class="sxs-lookup"><span data-stu-id="2d525-102">Q# Command Line Applications</span></span>

<span data-ttu-id="2d525-103">Os programas da Q # podem ser executados por conta própria, sem um driver em uma linguagem de host como C#, F # ou Python.</span><span class="sxs-lookup"><span data-stu-id="2d525-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="2d525-104">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2d525-104">Pre-requisites</span></span>

- [<span data-ttu-id="2d525-105">SDK do .NET Core 3,1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="2d525-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="2d525-106">Instalação</span><span class="sxs-lookup"><span data-stu-id="2d525-106">Installation</span></span>

<span data-ttu-id="2d525-107">Embora você possa criar aplicativos de linha de comando Q # em qualquer IDE, é altamente recomendável usar Visual Studio Code (VS Code) ou IDE do Visual Studio para seus aplicativos do Q #.</span><span class="sxs-lookup"><span data-stu-id="2d525-107">While you can build Q# command line applications in any IDE, we highly recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="2d525-108">Usando VS Code ou o Visual Studio e a extensão de Visual Studio Code QDK, você obterá acesso à funcionalidade mais rica.</span><span class="sxs-lookup"><span data-stu-id="2d525-108">By using VS Code or Visual Studio and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

- <span data-ttu-id="2d525-109">Instalar o [vs Code](https://code.visualstudio.com/download) (Windows, Linux e Mac)</span><span class="sxs-lookup"><span data-stu-id="2d525-109">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
- <span data-ttu-id="2d525-110">Instalar a [extensão QDK para vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) ou</span><span class="sxs-lookup"><span data-stu-id="2d525-110">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) OR</span></span>
- <span data-ttu-id="2d525-111">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, com a carga de trabalho de desenvolvimento multiplataforma com .NET Core habilitada</span><span class="sxs-lookup"><span data-stu-id="2d525-111">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>
- <span data-ttu-id="2d525-112">Baixar e instalar a [extensão do Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="2d525-112">Download and install the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="2d525-113">Desenvolver com Q # usando VS Code</span><span class="sxs-lookup"><span data-stu-id="2d525-113">Develop with Q# using VS Code</span></span>

<span data-ttu-id="2d525-114">Instale os modelos de projeto do Quantum:</span><span class="sxs-lookup"><span data-stu-id="2d525-114">Install the Quantum project templates:</span></span>

- <span data-ttu-id="2d525-115">Ir para **Exibir** -> **paleta de comandos**</span><span class="sxs-lookup"><span data-stu-id="2d525-115">Go to **View** -> **Command Palette**</span></span>
- <span data-ttu-id="2d525-116">Selecione **Q #: instalar modelos de projeto**</span><span class="sxs-lookup"><span data-stu-id="2d525-116">Select **Q#: Install project templates**</span></span>

<span data-ttu-id="2d525-117">Agora você tem o Quantum development kit instalado e pronto para uso em seus próprios aplicativos e suas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="2d525-117">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>
- <span data-ttu-id="2d525-118">Crie um novo projeto:</span><span class="sxs-lookup"><span data-stu-id="2d525-118">Create a new project:</span></span>
  - <span data-ttu-id="2d525-119">Ir para **Exibir** -> **paleta de comandos**</span><span class="sxs-lookup"><span data-stu-id="2d525-119">Go to **View** -> **Command Palette**</span></span>
  - <span data-ttu-id="2d525-120">Selecione **Q #: criar novo projeto**</span><span class="sxs-lookup"><span data-stu-id="2d525-120">Select **Q#: Create New Project**</span></span>
  - <span data-ttu-id="2d525-121">Selecionar **aplicativo de console autônomo**</span><span class="sxs-lookup"><span data-stu-id="2d525-121">Select **Standalone console application**</span></span>
  - <span data-ttu-id="2d525-122">Navegue até a localização no sistema de arquivos em que deseja criar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="2d525-122">Navigate to the location on the file system where you would like to create the application</span></span>
  - <span data-ttu-id="2d525-123">Clique no botão **Abrir novo projeto...** após a criação do projeto</span><span class="sxs-lookup"><span data-stu-id="2d525-123">Click on the **Open new project...** button, once the project has been created</span></span>
        
- <span data-ttu-id="2d525-124">Inspecionar o projeto</span><span class="sxs-lookup"><span data-stu-id="2d525-124">Inspect the project</span></span>
  - <span data-ttu-id="2d525-125">Você deve ver que um arquivo chamado `Program.qs` criado, que é um programa Q # que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="2d525-125">You should see that a file called `Program.qs` created, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

- <span data-ttu-id="2d525-126">Executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="2d525-126">Run the application:</span></span>
  - <span data-ttu-id="2d525-127">Ir para **terminal** -> **novo terminal**</span><span class="sxs-lookup"><span data-stu-id="2d525-127">Go to **Terminal** -> **New Terminal**</span></span>
  - <span data-ttu-id="2d525-128">Inserir `dotnet run`</span><span class="sxs-lookup"><span data-stu-id="2d525-128">Enter `dotnet run`</span></span>
  - <span data-ttu-id="2d525-129">Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="2d525-129">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> * <span data-ttu-id="2d525-130">No momento, não há suporte para workspaces com várias pastas raiz na extensão do Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="2d525-130">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="2d525-131">Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="2d525-131">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="2d525-132">Desenvolver com Q # usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2d525-132">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="2d525-133">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="2d525-133">Verify the installation by creating a `Hello World` application</span></span>

- <span data-ttu-id="2d525-134">Criar um aplicativo Q#</span><span class="sxs-lookup"><span data-stu-id="2d525-134">Create a new Q# application</span></span>
  - <span data-ttu-id="2d525-135">Ir para **arquivo** -> **novo** -> **projeto**</span><span class="sxs-lookup"><span data-stu-id="2d525-135">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="2d525-136">Digite `Q#` na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="2d525-136">Type `Q#` in the search box</span></span>
  - <span data-ttu-id="2d525-137">Selecione **Aplicativo Q#**</span><span class="sxs-lookup"><span data-stu-id="2d525-137">Select **Q# Application**</span></span>
  - <span data-ttu-id="2d525-138">Selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="2d525-138">Select **Next**</span></span>
  - <span data-ttu-id="2d525-139">Escolha um nome e uma localização para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="2d525-139">Choose a name and location for your application</span></span>
  - <span data-ttu-id="2d525-140">Selecione **criar**</span><span class="sxs-lookup"><span data-stu-id="2d525-140">Select **Create**</span></span>

- <span data-ttu-id="2d525-141">Inspecionar o projeto</span><span class="sxs-lookup"><span data-stu-id="2d525-141">Inspect the project</span></span>
  - <span data-ttu-id="2d525-142">Você verá que um arquivo chamado `Program.qs` foi criado, que é um programa Q # que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="2d525-142">You should see that a file called `Program.qs` has been created, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

- <span data-ttu-id="2d525-143">Executar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="2d525-143">Run the application</span></span>
  - <span data-ttu-id="2d525-144">Selecione **depurar** -> **Iniciar sem depuração**</span><span class="sxs-lookup"><span data-stu-id="2d525-144">Select **Debug** -> **Start Without Debugging**</span></span>
  - <span data-ttu-id="2d525-145">Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.</span><span class="sxs-lookup"><span data-stu-id="2d525-145">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="2d525-146">Caso você tenha vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas.</span><span class="sxs-lookup"><span data-stu-id="2d525-146">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  


## <a name="whats-next"></a><span data-ttu-id="2d525-147">O que vem a seguir?</span><span class="sxs-lookup"><span data-stu-id="2d525-147">What's next?</span></span>

<span data-ttu-id="2d525-148">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="2d525-148">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
