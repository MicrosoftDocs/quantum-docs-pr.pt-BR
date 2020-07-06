---
title: Desenvolver com aplicativos de linha de comando do Q#
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 15015d1673f47faf5a13dde516f834916b4319d6
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884278"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="ba357-102">Desenvolver com aplicativos de linha de comando do Q#</span><span class="sxs-lookup"><span data-stu-id="ba357-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="ba357-103">Os programas Q# podem ser executados por conta própria, sem um driver em uma linguagem de host como C#, F# ou Python.</span><span class="sxs-lookup"><span data-stu-id="ba357-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ba357-104">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ba357-104">Prerequisites</span></span>

- [<span data-ttu-id="ba357-105">SDK do .NET Core 3.1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ba357-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="ba357-106">Instalação</span><span class="sxs-lookup"><span data-stu-id="ba357-106">Installation</span></span>

<span data-ttu-id="ba357-107">Embora você possa compilar aplicativos de linha de comando do Q# em qualquer IDE, recomendamos usar o VS Code (Visual Studio Code) ou o IDE do Visual Studio para seus aplicativos Q#.</span><span class="sxs-lookup"><span data-stu-id="ba357-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="ba357-108">O desenvolvimento nesses ambientes inclui a funcionalidade sofisticada da extensão do QDK, que inclui avisos, realce de sintaxe, modelos de projeto e muito mais.</span><span class="sxs-lookup"><span data-stu-id="ba357-108">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="ba357-109">Para configurar o VS Code:</span><span class="sxs-lookup"><span data-stu-id="ba357-109">To configure VS Code:</span></span>

1. <span data-ttu-id="ba357-110">Baixe e instale o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).</span><span class="sxs-lookup"><span data-stu-id="ba357-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="ba357-111">Instale o [Microsoft QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="ba357-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="ba357-112">Para configurar o Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="ba357-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="ba357-113">Baixe e instale o [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 ou superior, com a carga de trabalho de desenvolvimento multiplataforma do .NET Core habilitada.</span><span class="sxs-lookup"><span data-stu-id="ba357-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="ba357-114">Baixe e instale o [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="ba357-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="ba357-115">Para instalar o QDK para outro ambiente, digite na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="ba357-115">To install the QDK for another environment, enter in the command line:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-q"></a><span data-ttu-id="ba357-116">Desenvolver com Q #</span><span class="sxs-lookup"><span data-stu-id="ba357-116">Develop with Q#</span></span>

<span data-ttu-id="ba357-117">Siga as instruções na guia correspondente ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="ba357-117">Follow the instructions at the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="ba357-118">Código do VS</span><span class="sxs-lookup"><span data-stu-id="ba357-118">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="ba357-119">Instale os modelos de projeto Q#:</span><span class="sxs-lookup"><span data-stu-id="ba357-119">Install the Q# project templates:</span></span>

1. <span data-ttu-id="ba357-120">Abra o VS Code.</span><span class="sxs-lookup"><span data-stu-id="ba357-120">Open VS Code.</span></span>
2. <span data-ttu-id="ba357-121">Clique em **Exibir** -> **Paleta de Comandos**.</span><span class="sxs-lookup"><span data-stu-id="ba357-121">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="ba357-122">Selecione **Q#: Instalar modelos de projeto**.</span><span class="sxs-lookup"><span data-stu-id="ba357-122">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="ba357-123">Quando a mensagem **Modelos de projeto instalados com êxito** for exibida, o QDK estará pronto para uso com bibliotecas e aplicativos próprios.</span><span class="sxs-lookup"><span data-stu-id="ba357-123">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="ba357-124">Para criar um projeto:</span><span class="sxs-lookup"><span data-stu-id="ba357-124">To create a new project:</span></span>

1. <span data-ttu-id="ba357-125">Clique em **Exibir** -> **Paleta de Comandos** e selecione **Q#: Criar Novo Projeto**.</span><span class="sxs-lookup"><span data-stu-id="ba357-125">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="ba357-126">Clique em **Aplicativo de console autônomo**.</span><span class="sxs-lookup"><span data-stu-id="ba357-126">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="ba357-127">Navegue até o local para salvar o projeto e clique em **Criar Projeto**.</span><span class="sxs-lookup"><span data-stu-id="ba357-127">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="ba357-128">Quando o projeto for criado com êxito, clique em **Abrir novo projeto...** no canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="ba357-128">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="ba357-129">Inspecione o projeto.</span><span class="sxs-lookup"><span data-stu-id="ba357-129">Inspect the project.</span></span> <span data-ttu-id="ba357-130">Você verá um arquivo de origem chamado `Program.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="ba357-130">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="ba357-131">Para executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="ba357-131">To run the application:</span></span>
1. <span data-ttu-id="ba357-132">Clique em **Terminal** -> **Novo Terminal**.</span><span class="sxs-lookup"><span data-stu-id="ba357-132">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="ba357-133">No prompt do terminal, insira `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="ba357-133">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="ba357-134">Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="ba357-134">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="ba357-135">No momento, não há suporte para workspaces com várias pastas raiz na extensão do Q# para VS Code.</span><span class="sxs-lookup"><span data-stu-id="ba357-135">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="ba357-136">Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="ba357-136">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="ba357-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ba357-137">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="ba357-138">Verifique sua instalação do Visual Studio criando um aplicativo Q# `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="ba357-138">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="ba357-139">Para criar um aplicativo Q#:</span><span class="sxs-lookup"><span data-stu-id="ba357-139">To create a new Q# application:</span></span>
1. <span data-ttu-id="ba357-140">Abra o Visual Studio e clique em **Arquivo** -> **Novo** -> **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="ba357-140">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="ba357-141">Digite `Q#` na caixa de pesquisa, selecione **Aplicativo Q#** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ba357-141">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="ba357-142">Insira um nome e um local para o aplicativo e clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="ba357-142">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="ba357-143">Inspecione o projeto.</span><span class="sxs-lookup"><span data-stu-id="ba357-143">Inspect the project.</span></span> <span data-ttu-id="ba357-144">Você verá um arquivo de origem chamado `Program.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="ba357-144">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="ba357-145">Para executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="ba357-145">To run the application:</span></span>
1. <span data-ttu-id="ba357-146">Selecione **Depurar** -> **Iniciar Sem Depuração**.</span><span class="sxs-lookup"><span data-stu-id="ba357-146">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="ba357-147">Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.</span><span class="sxs-lookup"><span data-stu-id="ba357-147">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="ba357-148">Se você tiver vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas dela.</span><span class="sxs-lookup"><span data-stu-id="ba357-148">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-line"></a>[<span data-ttu-id="ba357-149">Outros editores com a linha de comando</span><span class="sxs-lookup"><span data-stu-id="ba357-149">Other editors with the command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="ba357-150">Verifique sua instalação criando um aplicativo Q# `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="ba357-150">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="ba357-151">Crie um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="ba357-151">Create a new application:</span></span>
    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

2. <span data-ttu-id="ba357-152">Navegue até o diretório do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="ba357-152">Navigate to the application directory:</span></span>
    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="ba357-153">Agora, esse diretório deve conter um arquivo `Program.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="ba357-153">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="ba357-154">Você pode modificar esse modelo com um editor de texto e substituí-lo por seus aplicativos quânticos.</span><span class="sxs-lookup"><span data-stu-id="ba357-154">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

3. <span data-ttu-id="ba357-155">Execute o programa:</span><span class="sxs-lookup"><span data-stu-id="ba357-155">Run the program:</span></span>
    ```dotnetcli
    dotnet run
    ```

4. <span data-ttu-id="ba357-156">Você verá o seguinte texto impresso: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="ba357-156">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="ba357-157">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="ba357-157">Next steps</span></span>

<span data-ttu-id="ba357-158">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="ba357-158">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
