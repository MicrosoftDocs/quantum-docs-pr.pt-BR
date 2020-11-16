---
title: 'Desenvolver com aplicativos Q# em um IDE'
description: 'Saiba como criar um aplicativo Q# que é executado no prompt de comando.'
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: a6823888dcbe8cf79f0045d2615fe8b889dcc7c3
ms.sourcegitcommit: a13c7c86fd52a05cbf129b8dd713d6586ca1cc2c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "93376415"
---
# <a name="develop-with-no-locq-applications-in-an-ide"></a><span data-ttu-id="80838-103">Desenvolver com aplicativos Q# em um IDE</span><span class="sxs-lookup"><span data-stu-id="80838-103">Develop with Q# applications in an IDE</span></span>

<span data-ttu-id="80838-104">Os programas Q# podem ser executados por conta própria em uma linguagem de host, como C#, F# ou Python, sem a necessidade de um driver.</span><span class="sxs-lookup"><span data-stu-id="80838-104">Q# programs can run on their own, without a driver in a host language like C#, F#, or Python.</span></span> <span data-ttu-id="80838-105">Você pode desenvolver aplicativos Q# no VS Code (Visual Studio Code), no Visual Studio, nos Codespaces do Visual Studio ou em qualquer editor/IDE e executar aplicativos no console do .NET.</span><span class="sxs-lookup"><span data-stu-id="80838-105">You can develop Q# applications in Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces, or with any editor/IDE and run applications from the .NET console.</span></span> 

## <a name="prerequisites-for-all-environments"></a><span data-ttu-id="80838-106">Pré-requisitos para todos os ambientes</span><span class="sxs-lookup"><span data-stu-id="80838-106">Prerequisites for all environments</span></span>

- [<span data-ttu-id="80838-107">SDK do .NET Core 3.1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="80838-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="80838-108">Instalação</span><span class="sxs-lookup"><span data-stu-id="80838-108">Installation</span></span>

<span data-ttu-id="80838-109">Embora seja possível compilar aplicativos Q# em qualquer IDE, é recomendável usar o VS Code (Visual Studio Code) ou o IDE do Visual Studio para desenvolver aplicativos Q# localmente.</span><span class="sxs-lookup"><span data-stu-id="80838-109">While you can build Q# applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="80838-110">Para desenvolvimento na nuvem por meio do navegador da Web, recomendamos o Codespaces do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="80838-110">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="80838-111">O desenvolvimento nesses ambientes permite aproveitar a funcionalidade sofisticada da extensão do QDK, que inclui avisos, realce de sintaxe, modelos de projeto e muito mais.</span><span class="sxs-lookup"><span data-stu-id="80838-111">Developing in these environments leverages the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

### <a name="to-configure-for-vs-code"></a><span data-ttu-id="80838-112">Para configurar para o VS Code:</span><span class="sxs-lookup"><span data-stu-id="80838-112">To configure for VS Code:</span></span>

1. <span data-ttu-id="80838-113">Baixe e instale o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).</span><span class="sxs-lookup"><span data-stu-id="80838-113">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="80838-114">Instale o [Microsoft QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="80838-114">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

### <a name="to-configure-for-visual-studio"></a><span data-ttu-id="80838-115">Para configurar para o Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="80838-115">To configure for Visual Studio:</span></span>

1. <span data-ttu-id="80838-116">Baixe e instale o [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 ou superior, com a carga de trabalho de desenvolvimento multiplataforma do .NET Core habilitada.</span><span class="sxs-lookup"><span data-stu-id="80838-116">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="80838-117">Baixe e instale o [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="80838-117">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

### <a name="to-configure-for-another-environment"></a><span data-ttu-id="80838-118">Para configurar para outro ambiente:</span><span class="sxs-lookup"><span data-stu-id="80838-118">To configure for another environment:</span></span> 

1. <span data-ttu-id="80838-119">Digite o seguinte no prompt de comando</span><span class="sxs-lookup"><span data-stu-id="80838-119">Enter the following at the command prompt</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

### <a name="to-configure-for-visual-studio-codespaces"></a><span data-ttu-id="80838-120">Para configurar para os Codespaces do Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="80838-120">To configure for Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="80838-121">Criar uma [conta do Azure](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="80838-121">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="80838-122">Crie um ambiente de Codespaces.</span><span class="sxs-lookup"><span data-stu-id="80838-122">Create a Codespaces environment.</span></span> <span data-ttu-id="80838-123">Siga o [guia de início rápido](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span><span class="sxs-lookup"><span data-stu-id="80838-123">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span></span> <span data-ttu-id="80838-124">Ao criar o espaço de código, é recomendável inserir `microsoft/Quantum` no campo "Repositório Git" para carregar configurações específicas do QDK.</span><span class="sxs-lookup"><span data-stu-id="80838-124">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="80838-125">Agora você pode iniciar o novo ambiente e começar a desenvolver no navegador por meio do [IDE de nuvem do Codespaces do VS](https://online.visualstudio.com/environments).</span><span class="sxs-lookup"><span data-stu-id="80838-125">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="80838-126">Como alternativa, é possível usar a instalação local do VS Code e usar o Codespaces como um [ambiente remoto](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span><span class="sxs-lookup"><span data-stu-id="80838-126">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>

## <a name="develop-with-no-locq"></a><span data-ttu-id="80838-127">Desenvolver com Q#</span><span class="sxs-lookup"><span data-stu-id="80838-127">Develop with Q#</span></span>

<span data-ttu-id="80838-128">Siga as instruções na guia correspondente ao seu ambiente de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="80838-128">Follow the instructions on the tab corresponding to your development environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="80838-129">Código do VS</span><span class="sxs-lookup"><span data-stu-id="80838-129">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="80838-130">Para criar um projeto:</span><span class="sxs-lookup"><span data-stu-id="80838-130">To create a new project:</span></span>

1. <span data-ttu-id="80838-131">Clique em **Exibir** -> **Paleta de Comandos** e selecione **Q#: Criar Novo Projeto**.</span><span class="sxs-lookup"><span data-stu-id="80838-131">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="80838-132">Clique em **Aplicativo de console autônomo**.</span><span class="sxs-lookup"><span data-stu-id="80838-132">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="80838-133">Navegue até o local para salvar o projeto e clique em **Criar Projeto**.</span><span class="sxs-lookup"><span data-stu-id="80838-133">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="80838-134">Quando o projeto for criado com êxito, clique em **Abrir novo projeto...** no canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="80838-134">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="80838-135">Inspecione o projeto.</span><span class="sxs-lookup"><span data-stu-id="80838-135">Inspect the project.</span></span> <span data-ttu-id="80838-136">Você verá um arquivo de origem chamado `Program.qs`, um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="80838-136">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="80838-137">Para executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="80838-137">To run the application:</span></span>

1. <span data-ttu-id="80838-138">Clique em **Terminal** -> **Novo Terminal**.</span><span class="sxs-lookup"><span data-stu-id="80838-138">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="80838-139">No prompt do terminal, insira `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="80838-139">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="80838-140">Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="80838-140">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> <span data-ttu-id="80838-141">No momento, não há compatibilidade com workspaces com várias pastas raiz na extensão do Q# para VS Code.</span><span class="sxs-lookup"><span data-stu-id="80838-141">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="80838-142">Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="80838-142">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="80838-143">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="80838-143">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="80838-144">Verifique sua instalação do Visual Studio criando um aplicativo Q# `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="80838-144">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="80838-145">Para criar um novo aplicativo Q#:</span><span class="sxs-lookup"><span data-stu-id="80838-145">To create a new Q# application:</span></span>

1. <span data-ttu-id="80838-146">Abra o Visual Studio e clique em **Arquivo** -> **Novo** -> **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="80838-146">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="80838-147">Digite `Q#` na caixa de pesquisa, selecione **Aplicativo Q#** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="80838-147">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="80838-148">Insira um nome e um local para o aplicativo e clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="80838-148">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="80838-149">Inspecione o projeto.</span><span class="sxs-lookup"><span data-stu-id="80838-149">Inspect the project.</span></span> <span data-ttu-id="80838-150">Você verá um arquivo de origem chamado `Program.qs`, um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="80838-150">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="80838-151">Para executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="80838-151">To run the application:</span></span>

1. <span data-ttu-id="80838-152">Selecione **Depurar** -> **Iniciar Sem Depuração**.</span><span class="sxs-lookup"><span data-stu-id="80838-152">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="80838-153">Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.</span><span class="sxs-lookup"><span data-stu-id="80838-153">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="80838-154">Se você tiver vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas dela.</span><span class="sxs-lookup"><span data-stu-id="80838-154">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="80838-155">Outros editores com o prompt de comando</span><span class="sxs-lookup"><span data-stu-id="80838-155">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="80838-156">Verifique sua instalação criando um aplicativo Q# `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="80838-156">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="80838-157">Crie um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="80838-157">Create a new application:</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="80838-158">Navegue até o diretório do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="80838-158">Navigate to the application directory:</span></span>

    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="80838-159">Agora, esse diretório deve conter um arquivo `Program.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="80838-159">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="80838-160">Você pode modificar esse modelo com um editor de texto e substituí-lo por seus aplicativos quânticos.</span><span class="sxs-lookup"><span data-stu-id="80838-160">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="80838-161">Execute o programa:</span><span class="sxs-lookup"><span data-stu-id="80838-161">Run the program:</span></span>

    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="80838-162">Você verá o seguinte texto impresso: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="80838-162">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="80838-163">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="80838-163">Next steps</span></span>

<span data-ttu-id="80838-164">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="80838-164">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
