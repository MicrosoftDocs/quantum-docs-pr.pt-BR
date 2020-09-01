---
title: Desenvolver com aplicativos Q#
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6a287dd76162a05d72af7e9d1e46533425283e2a
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863655"
---
# <a name="develop-with-no-locq-applications"></a><span data-ttu-id="9c616-102">Desenvolver com aplicativos Q#</span><span class="sxs-lookup"><span data-stu-id="9c616-102">Develop with Q# applications</span></span>

<span data-ttu-id="9c616-103">Os programas Q# podem ser executados por conta própria, sem um driver em uma linguagem de host como C#, F# ou Python.</span><span class="sxs-lookup"><span data-stu-id="9c616-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9c616-104">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9c616-104">Prerequisites</span></span>

- [<span data-ttu-id="9c616-105">SDK do .NET Core 3.1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9c616-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="9c616-106">Instalação</span><span class="sxs-lookup"><span data-stu-id="9c616-106">Installation</span></span>

<span data-ttu-id="9c616-107">Embora seja possível compilar aplicativos Q# em qualquer IDE, é recomendável usar o VS Code (Visual Studio Code) ou o IDE do Visual Studio para desenvolver aplicativos Q# localmente.</span><span class="sxs-lookup"><span data-stu-id="9c616-107">While you can build Q# applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="9c616-108">Para desenvolvimento na nuvem por meio do navegador da Web, recomendamos o Codespaces do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9c616-108">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="9c616-109">O desenvolvimento nesses ambientes inclui a funcionalidade sofisticada da extensão do QDK, que inclui avisos, realce de sintaxe, modelos de projeto e muito mais.</span><span class="sxs-lookup"><span data-stu-id="9c616-109">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

<span data-ttu-id="9c616-110">Para configurar o VS Code:</span><span class="sxs-lookup"><span data-stu-id="9c616-110">To configure VS Code:</span></span>

1. <span data-ttu-id="9c616-111">Baixe e instale o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).</span><span class="sxs-lookup"><span data-stu-id="9c616-111">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="9c616-112">Instale o [Microsoft QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="9c616-112">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="9c616-113">Para configurar o Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="9c616-113">To configure Visual Studio:</span></span>

1. <span data-ttu-id="9c616-114">Baixe e instale o [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 ou superior, com a carga de trabalho de desenvolvimento multiplataforma do .NET Core habilitada.</span><span class="sxs-lookup"><span data-stu-id="9c616-114">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="9c616-115">Baixe e instale o [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="9c616-115">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="9c616-116">Para configurar o Codespaces do Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="9c616-116">To configure Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="9c616-117">Criar uma [conta do Azure](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="9c616-117">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="9c616-118">Crie um ambiente de Codespaces.</span><span class="sxs-lookup"><span data-stu-id="9c616-118">Create a Codespaces environment.</span></span> <span data-ttu-id="9c616-119">Siga o [guia de início rápido](https://docs.microsoft.com/visualstudio/online/quickstarts/browser).</span><span class="sxs-lookup"><span data-stu-id="9c616-119">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/online/quickstarts/browser).</span></span> <span data-ttu-id="9c616-120">Ao criar o espaço de código, é recomendável inserir `microsoft/Quantum` no campo "Repositório Git" para carregar configurações específicas do QDK.</span><span class="sxs-lookup"><span data-stu-id="9c616-120">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="9c616-121">Agora você pode iniciar o novo ambiente e começar a desenvolver no navegador por meio do [IDE de nuvem do Codespaces do VS](https://online.visualstudio.com/environments).</span><span class="sxs-lookup"><span data-stu-id="9c616-121">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="9c616-122">Como alternativa, é possível usar a instalação local do VS Code e usar o Codespaces como um [ambiente remoto](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span><span class="sxs-lookup"><span data-stu-id="9c616-122">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>


<span data-ttu-id="9c616-123">Para instalar o QDK para outro ambiente, digite no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="9c616-123">To install the QDK for another environment, enter at the command prompt:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-no-locq"></a><span data-ttu-id="9c616-124">Desenvolver com Q#</span><span class="sxs-lookup"><span data-stu-id="9c616-124">Develop with Q#</span></span>

<span data-ttu-id="9c616-125">Siga as instruções na guia correspondente ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="9c616-125">Follow the instructions at the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="9c616-126">Código do VS</span><span class="sxs-lookup"><span data-stu-id="9c616-126">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="9c616-127">Para criar um projeto:</span><span class="sxs-lookup"><span data-stu-id="9c616-127">To create a new project:</span></span>

1. <span data-ttu-id="9c616-128">Clique em **Exibir** -> **Paleta de Comandos** e selecione **Q#: Criar Novo Projeto**.</span><span class="sxs-lookup"><span data-stu-id="9c616-128">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="9c616-129">Clique em **Aplicativo de console autônomo**.</span><span class="sxs-lookup"><span data-stu-id="9c616-129">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="9c616-130">Navegue até o local para salvar o projeto e clique em **Criar Projeto**.</span><span class="sxs-lookup"><span data-stu-id="9c616-130">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="9c616-131">Quando o projeto for criado com êxito, clique em **Abrir novo projeto...** no canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="9c616-131">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="9c616-132">Inspecione o projeto.</span><span class="sxs-lookup"><span data-stu-id="9c616-132">Inspect the project.</span></span> <span data-ttu-id="9c616-133">Você verá um arquivo de origem chamado `Program.qs`, um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="9c616-133">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="9c616-134">Para executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="9c616-134">To run the application:</span></span>
1. <span data-ttu-id="9c616-135">Clique em **Terminal** -> **Novo Terminal**.</span><span class="sxs-lookup"><span data-stu-id="9c616-135">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="9c616-136">No prompt do terminal, insira `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="9c616-136">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="9c616-137">Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="9c616-137">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="9c616-138">No momento, não há compatibilidade com workspaces com várias pastas raiz na extensão do Q# para VS Code.</span><span class="sxs-lookup"><span data-stu-id="9c616-138">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="9c616-139">Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="9c616-139">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="9c616-140">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9c616-140">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="9c616-141">Verifique sua instalação do Visual Studio criando um aplicativo Q# `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="9c616-141">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="9c616-142">Para criar um novo aplicativo Q#:</span><span class="sxs-lookup"><span data-stu-id="9c616-142">To create a new Q# application:</span></span>
1. <span data-ttu-id="9c616-143">Abra o Visual Studio e clique em **Arquivo** -> **Novo** -> **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="9c616-143">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="9c616-144">Digite `Q#` na caixa de pesquisa, selecione **Aplicativo Q#** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9c616-144">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="9c616-145">Insira um nome e um local para o aplicativo e clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="9c616-145">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="9c616-146">Inspecione o projeto.</span><span class="sxs-lookup"><span data-stu-id="9c616-146">Inspect the project.</span></span> <span data-ttu-id="9c616-147">Você verá um arquivo de origem chamado `Program.qs`, um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="9c616-147">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="9c616-148">Para executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="9c616-148">To run the application:</span></span>
1. <span data-ttu-id="9c616-149">Selecione **Depurar** -> **Iniciar Sem Depuração**.</span><span class="sxs-lookup"><span data-stu-id="9c616-149">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="9c616-150">Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.</span><span class="sxs-lookup"><span data-stu-id="9c616-150">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="9c616-151">Se você tiver vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas dela.</span><span class="sxs-lookup"><span data-stu-id="9c616-151">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="9c616-152">Outros editores com o prompt de comando</span><span class="sxs-lookup"><span data-stu-id="9c616-152">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="9c616-153">Verifique sua instalação criando um aplicativo Q# `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="9c616-153">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="9c616-154">Instale os modelos de projeto.</span><span class="sxs-lookup"><span data-stu-id="9c616-154">Install the project templates.</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="9c616-155">Crie um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="9c616-155">Create a new application:</span></span>
    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="9c616-156">Navegue até o diretório do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="9c616-156">Navigate to the application directory:</span></span>
    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="9c616-157">Agora, esse diretório deve conter um arquivo `Program.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="9c616-157">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="9c616-158">Você pode modificar esse modelo com um editor de texto e substituí-lo por seus aplicativos quânticos.</span><span class="sxs-lookup"><span data-stu-id="9c616-158">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="9c616-159">Execute o programa:</span><span class="sxs-lookup"><span data-stu-id="9c616-159">Run the program:</span></span>
    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="9c616-160">Você verá o seguinte texto impresso: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="9c616-160">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="9c616-161">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9c616-161">Next steps</span></span>

<span data-ttu-id="9c616-162">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="9c616-162">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
