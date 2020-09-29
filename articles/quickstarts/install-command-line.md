---
title: Desenvolver com aplicativos Q#
description: Saiba como criar um aplicativo Q# que é executado no prompt de comando.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 68f530d80e5c5f40dc2bcbb185879c3cb6f93f91
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834407"
---
# <a name="develop-with-no-locq-applications"></a><span data-ttu-id="bf84d-103">Desenvolver com aplicativos Q#</span><span class="sxs-lookup"><span data-stu-id="bf84d-103">Develop with Q# applications</span></span>

<span data-ttu-id="bf84d-104">Siga as instruções na guia correspondente ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="bf84d-104">Follow the instructions at the tab corresponding to your environment.</span></span>

<span data-ttu-id="bf84d-105">Os programas Q# podem ser executados por conta própria em uma linguagem de host, como C#, F# ou Python, sem a necessidade de um driver.</span><span class="sxs-lookup"><span data-stu-id="bf84d-105">Q# programs can run on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bf84d-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="bf84d-106">Prerequisites</span></span>

- [<span data-ttu-id="bf84d-107">SDK do .NET Core 3.1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="bf84d-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="bf84d-108">Instalação</span><span class="sxs-lookup"><span data-stu-id="bf84d-108">Installation</span></span>

<span data-ttu-id="bf84d-109">Embora seja possível compilar aplicativos Q# em qualquer IDE, é recomendável usar o VS Code (Visual Studio Code) ou o IDE do Visual Studio para desenvolver aplicativos Q# localmente.</span><span class="sxs-lookup"><span data-stu-id="bf84d-109">While you can build Q# applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="bf84d-110">Para desenvolvimento na nuvem por meio do navegador da Web, recomendamos o Codespaces do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bf84d-110">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="bf84d-111">O desenvolvimento nesses ambientes inclui a funcionalidade sofisticada da extensão do QDK, que inclui avisos, realce de sintaxe, modelos de projeto e muito mais.</span><span class="sxs-lookup"><span data-stu-id="bf84d-111">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

<span data-ttu-id="bf84d-112">Para configurar o VS Code:</span><span class="sxs-lookup"><span data-stu-id="bf84d-112">To configure VS Code:</span></span>

1. <span data-ttu-id="bf84d-113">Baixe e instale o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).</span><span class="sxs-lookup"><span data-stu-id="bf84d-113">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="bf84d-114">Instale o [Microsoft QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="bf84d-114">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="bf84d-115">Para configurar o Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="bf84d-115">To configure Visual Studio:</span></span>

1. <span data-ttu-id="bf84d-116">Baixe e instale o [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 ou superior, com a carga de trabalho de desenvolvimento multiplataforma do .NET Core habilitada.</span><span class="sxs-lookup"><span data-stu-id="bf84d-116">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="bf84d-117">Baixe e instale o [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="bf84d-117">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="bf84d-118">Para configurar o Codespaces do Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="bf84d-118">To configure Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="bf84d-119">Criar uma [conta do Azure](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="bf84d-119">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="bf84d-120">Crie um ambiente de Codespaces.</span><span class="sxs-lookup"><span data-stu-id="bf84d-120">Create a Codespaces environment.</span></span> <span data-ttu-id="bf84d-121">Siga o [guia de início rápido](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span><span class="sxs-lookup"><span data-stu-id="bf84d-121">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span></span> <span data-ttu-id="bf84d-122">Ao criar o espaço de código, é recomendável inserir `microsoft/Quantum` no campo "Repositório Git" para carregar configurações específicas do QDK.</span><span class="sxs-lookup"><span data-stu-id="bf84d-122">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="bf84d-123">Agora você pode iniciar o novo ambiente e começar a desenvolver no navegador por meio do [IDE de nuvem do Codespaces do VS](https://online.visualstudio.com/environments).</span><span class="sxs-lookup"><span data-stu-id="bf84d-123">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="bf84d-124">Como alternativa, é possível usar a instalação local do VS Code e usar o Codespaces como um [ambiente remoto](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span><span class="sxs-lookup"><span data-stu-id="bf84d-124">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>


<span data-ttu-id="bf84d-125">Para instalar o QDK em outro ambiente, digite o seguinte no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="bf84d-125">To install the QDK for another environment, enter the following at the command prompt:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-no-locq"></a><span data-ttu-id="bf84d-126">Desenvolver com Q#</span><span class="sxs-lookup"><span data-stu-id="bf84d-126">Develop with Q#</span></span>

<span data-ttu-id="bf84d-127">Siga as instruções na guia correspondente ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="bf84d-127">Follow the instructions on the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="bf84d-128">Código do VS</span><span class="sxs-lookup"><span data-stu-id="bf84d-128">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="bf84d-129">Para criar um projeto:</span><span class="sxs-lookup"><span data-stu-id="bf84d-129">To create a new project:</span></span>

1. <span data-ttu-id="bf84d-130">Clique em **Exibir** -> **Paleta de Comandos** e selecione **Q#: Criar Novo Projeto**.</span><span class="sxs-lookup"><span data-stu-id="bf84d-130">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="bf84d-131">Clique em **Aplicativo de console autônomo**.</span><span class="sxs-lookup"><span data-stu-id="bf84d-131">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="bf84d-132">Navegue até o local para salvar o projeto e clique em **Criar Projeto**.</span><span class="sxs-lookup"><span data-stu-id="bf84d-132">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="bf84d-133">Quando o projeto for criado com êxito, clique em **Abrir novo projeto...** no canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="bf84d-133">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="bf84d-134">Inspecione o projeto.</span><span class="sxs-lookup"><span data-stu-id="bf84d-134">Inspect the project.</span></span> <span data-ttu-id="bf84d-135">Você verá um arquivo de origem chamado `Program.qs`, um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="bf84d-135">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="bf84d-136">Para executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="bf84d-136">To run the application:</span></span>

1. <span data-ttu-id="bf84d-137">Clique em **Terminal** -> **Novo Terminal**.</span><span class="sxs-lookup"><span data-stu-id="bf84d-137">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="bf84d-138">No prompt do terminal, insira `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="bf84d-138">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="bf84d-139">Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="bf84d-139">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> <span data-ttu-id="bf84d-140">No momento, não há compatibilidade com workspaces com várias pastas raiz na extensão do Q# para VS Code.</span><span class="sxs-lookup"><span data-stu-id="bf84d-140">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="bf84d-141">Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="bf84d-141">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="bf84d-142">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bf84d-142">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="bf84d-143">Verifique sua instalação do Visual Studio criando um aplicativo Q# `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="bf84d-143">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="bf84d-144">Para criar um novo aplicativo Q#:</span><span class="sxs-lookup"><span data-stu-id="bf84d-144">To create a new Q# application:</span></span>

1. <span data-ttu-id="bf84d-145">Abra o Visual Studio e clique em **Arquivo** -> **Novo** -> **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="bf84d-145">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="bf84d-146">Digite `Q#` na caixa de pesquisa, selecione **Aplicativo Q#** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bf84d-146">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="bf84d-147">Insira um nome e um local para o aplicativo e clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="bf84d-147">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="bf84d-148">Inspecione o projeto.</span><span class="sxs-lookup"><span data-stu-id="bf84d-148">Inspect the project.</span></span> <span data-ttu-id="bf84d-149">Você verá um arquivo de origem chamado `Program.qs`, um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="bf84d-149">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="bf84d-150">Para executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="bf84d-150">To run the application:</span></span>

1. <span data-ttu-id="bf84d-151">Selecione **Depurar** -> **Iniciar Sem Depuração**.</span><span class="sxs-lookup"><span data-stu-id="bf84d-151">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="bf84d-152">Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.</span><span class="sxs-lookup"><span data-stu-id="bf84d-152">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="bf84d-153">Se você tiver vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas dela.</span><span class="sxs-lookup"><span data-stu-id="bf84d-153">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="bf84d-154">Outros editores com o prompt de comando</span><span class="sxs-lookup"><span data-stu-id="bf84d-154">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="bf84d-155">Verifique sua instalação criando um aplicativo Q# `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="bf84d-155">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="bf84d-156">Instale os modelos de projeto.</span><span class="sxs-lookup"><span data-stu-id="bf84d-156">Install the project templates.</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="bf84d-157">Crie um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="bf84d-157">Create a new application:</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="bf84d-158">Navegue até o diretório do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="bf84d-158">Navigate to the application directory:</span></span>

    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="bf84d-159">Agora, esse diretório deve conter um arquivo `Program.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="bf84d-159">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="bf84d-160">Você pode modificar esse modelo com um editor de texto e substituí-lo por seus aplicativos quânticos.</span><span class="sxs-lookup"><span data-stu-id="bf84d-160">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="bf84d-161">Execute o programa:</span><span class="sxs-lookup"><span data-stu-id="bf84d-161">Run the program:</span></span>

    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="bf84d-162">Você verá o seguinte texto impresso: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="bf84d-162">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="bf84d-163">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="bf84d-163">Next steps</span></span>

<span data-ttu-id="bf84d-164">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="bf84d-164">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
