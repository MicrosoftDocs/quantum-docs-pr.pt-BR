---
title: 'Desenvolver com Q # +C#'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 7803846279f230f5fc0ee8424bd39be735a650ca
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036280"
---
# <a name="develop-with-q--c"></a><span data-ttu-id="9725e-102">Desenvolver com Q # +C#</span><span class="sxs-lookup"><span data-stu-id="9725e-102">Develop with Q# + C#</span></span>

<span data-ttu-id="9725e-103">Instale o QDK para desenvolver C# programas de host para chamar Q # operações.</span><span class="sxs-lookup"><span data-stu-id="9725e-103">Install the QDK to develop C# host programs to call Q# operations.</span></span>

<span data-ttu-id="9725e-104">O Q # foi criado para brincar bem com linguagens .NET – C#especificamente.</span><span class="sxs-lookup"><span data-stu-id="9725e-104">Q# is built to play well with .NET languages--specifically C#.</span></span> <span data-ttu-id="9725e-105">Você pode trabalhar com esse emparelhamento dentro de diferentes ambientes de desenvolvimento:</span><span class="sxs-lookup"><span data-stu-id="9725e-105">You can work with this pairing inside different development environments:</span></span>

- [<span data-ttu-id="9725e-106">Q # + C# usando o Visual Studio (Windows)</span><span class="sxs-lookup"><span data-stu-id="9725e-106">Q# + C# using Visual Studio (Windows)</span></span>](#VS)
- [<span data-ttu-id="9725e-107">Q # + C# usando Visual Studio Code (Windows, Linux e Mac)</span><span class="sxs-lookup"><span data-stu-id="9725e-107">Q# + C# using Visual Studio Code (Windows, Linux and Mac)</span></span>](#VSC)
- [<span data-ttu-id="9725e-108">Q # + C# usando a ferramenta de linha de comando `dotnet`</span><span class="sxs-lookup"><span data-stu-id="9725e-108">Q# + C# using the `dotnet` command-line tool</span></span>](#command)

## <span data-ttu-id="9725e-109">Desenvolver com Q # + C# usando o Visual Studio <a name="VS"></a></span><span class="sxs-lookup"><span data-stu-id="9725e-109">Develop with Q# + C# using Visual Studio <a name="VS"></a></span></span>

<span data-ttu-id="9725e-110">O Visual Studio oferece um ambiente avançado para o desenvolvimento de programas em Q #.</span><span class="sxs-lookup"><span data-stu-id="9725e-110">Visual Studio offers a rich environment for developing Q# programs.</span></span> <span data-ttu-id="9725e-111">A extensão do Visual Studio para Q # contém modelos para arquivos e projetos do Q #, bem como realce de sintaxe, conclusão de código e suporte IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="9725e-111">The Q# Visual Studio extension contains templates for Q# files and projects as well as syntax highlighting, code completion and IntelliSense support.</span></span>


1. <span data-ttu-id="9725e-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9725e-112">Pre-requisites</span></span>

    - <span data-ttu-id="9725e-113">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, com a carga de trabalho de desenvolvimento multiplataforma com .NET Core habilitada</span><span class="sxs-lookup"><span data-stu-id="9725e-113">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="9725e-114">Instalar a extensão do Visual Studio para Q#</span><span class="sxs-lookup"><span data-stu-id="9725e-114">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="9725e-115">Baixar e instalar a [extensão do Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="9725e-115">Download and install the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>

1. <span data-ttu-id="9725e-116">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="9725e-116">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="9725e-117">Criar um aplicativo Q#</span><span class="sxs-lookup"><span data-stu-id="9725e-117">Create a new Q# application</span></span>

        - <span data-ttu-id="9725e-118">Acesse **Arquivo** -> **Novo** -> **Projeto**</span><span class="sxs-lookup"><span data-stu-id="9725e-118">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="9725e-119">Digite `Q#` na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="9725e-119">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="9725e-120">Selecione **Aplicativo Q#**</span><span class="sxs-lookup"><span data-stu-id="9725e-120">Select **Q# Application**</span></span>
        - <span data-ttu-id="9725e-121">Selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9725e-121">Select **Next**</span></span>
        - <span data-ttu-id="9725e-122">Escolha um nome e uma localização para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="9725e-122">Choose a name and location for your application</span></span>
        - <span data-ttu-id="9725e-123">Escolha **Criar**</span><span class="sxs-lookup"><span data-stu-id="9725e-123">Select **Create**</span></span>

    - <span data-ttu-id="9725e-124">Inspecionar o projeto</span><span class="sxs-lookup"><span data-stu-id="9725e-124">Inspect the project</span></span>

        <span data-ttu-id="9725e-125">Você deverá ver que dois arquivos foram criados: `Driver.cs`, que é o aplicativo host C#; e `Operation.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="9725e-125">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="9725e-126">Executar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="9725e-126">Run the application</span></span>

        - <span data-ttu-id="9725e-127">Selecione **Depurar** -> **Iniciar Sem Depuração**</span><span class="sxs-lookup"><span data-stu-id="9725e-127">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="9725e-128">Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.</span><span class="sxs-lookup"><span data-stu-id="9725e-128">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="9725e-129">Caso você tenha vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas.</span><span class="sxs-lookup"><span data-stu-id="9725e-129">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <span data-ttu-id="9725e-130">Desenvolver com Q # + C# usando Visual Studio Code <a name="VSC"></a></span><span class="sxs-lookup"><span data-stu-id="9725e-130">Develop with Q# + C# using Visual Studio Code <a name="VSC"></a></span></span>

<span data-ttu-id="9725e-131">O Visual Studio Code (VS Code) oferece um ambiente avançado para o desenvolvimento de programas em Q # no Windows, Linux e Mac.</span><span class="sxs-lookup"><span data-stu-id="9725e-131">Visual Studio Code (VS Code) offers a rich environment for developing Q# programs on Windows, Linux and Mac.</span></span>  <span data-ttu-id="9725e-132">A extensão Q # VS Code inclui suporte para realce de sintaxe Q #, conclusão de código e trechos de código Q #.</span><span class="sxs-lookup"><span data-stu-id="9725e-132">The Q# VS Code extension includes support for Q# syntax highlighting, code completion, and Q# code snippets.</span></span>

1. <span data-ttu-id="9725e-133">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9725e-133">Pre-requisites</span></span>

   - [<span data-ttu-id="9725e-134">Código do VS</span><span class="sxs-lookup"><span data-stu-id="9725e-134">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="9725e-135">SDK do .NET Core 3,1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9725e-135">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="9725e-136">Instalar a extensão do VS Code para Quantum</span><span class="sxs-lookup"><span data-stu-id="9725e-136">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="9725e-137">Instalar a [extensão do VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span><span class="sxs-lookup"><span data-stu-id="9725e-137">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="9725e-138">Instale os modelos de projeto do Quantum:</span><span class="sxs-lookup"><span data-stu-id="9725e-138">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="9725e-139">Acesse **Exibir** -> **Paleta de Comandos**</span><span class="sxs-lookup"><span data-stu-id="9725e-139">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="9725e-140">Selecione **Q #: instalar modelos de projeto**</span><span class="sxs-lookup"><span data-stu-id="9725e-140">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="9725e-141">Agora você tem o Quantum development kit instalado e pronto para uso em seus próprios aplicativos e suas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="9725e-141">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="9725e-142">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="9725e-142">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="9725e-143">Crie um novo projeto:</span><span class="sxs-lookup"><span data-stu-id="9725e-143">Create a new project:</span></span>

        - <span data-ttu-id="9725e-144">Acesse **Exibir** -> **Paleta de Comandos**</span><span class="sxs-lookup"><span data-stu-id="9725e-144">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="9725e-145">Selecione **Q #: criar novo projeto**</span><span class="sxs-lookup"><span data-stu-id="9725e-145">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="9725e-146">Selecionar **aplicativo de console autônomo**</span><span class="sxs-lookup"><span data-stu-id="9725e-146">Select **Standalone console application**</span></span>
        - <span data-ttu-id="9725e-147">Navegue até a localização no sistema de arquivos em que deseja criar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="9725e-147">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="9725e-148">Clique no botão **Abrir novo projeto...** após a criação do projeto</span><span class="sxs-lookup"><span data-stu-id="9725e-148">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="9725e-149">Se você ainda não tiver a C# extensão para vs Code instalada, um pop-up será exibido.</span><span class="sxs-lookup"><span data-stu-id="9725e-149">If you don't already have the C# extension for VS Code installed, a pop-up will appear.</span></span> <span data-ttu-id="9725e-150">Instale a extensão.</span><span class="sxs-lookup"><span data-stu-id="9725e-150">Install the extension.</span></span> 

    - <span data-ttu-id="9725e-151">Executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="9725e-151">Run the application:</span></span>

        - <span data-ttu-id="9725e-152">Ir para **terminal** -> **novo terminal**</span><span class="sxs-lookup"><span data-stu-id="9725e-152">Go to **Terminal** -> **New Terminal**</span></span>
        - <span data-ttu-id="9725e-153">Inserir `dotnet run`</span><span class="sxs-lookup"><span data-stu-id="9725e-153">Enter `dotnet run`</span></span>
        - <span data-ttu-id="9725e-154">Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="9725e-154">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> * <span data-ttu-id="9725e-155">No momento, não há suporte para workspaces com várias pastas raiz na extensão do Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="9725e-155">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="9725e-156">Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="9725e-156">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <span data-ttu-id="9725e-157">Desenvolver com Q # + C# usando a ferramenta de linha de comando `dotnet`<a name="command"></a></span><span class="sxs-lookup"><span data-stu-id="9725e-157">Develop with Q# + C# using the `dotnet` command-line tool <a name="command"></a></span></span>

<span data-ttu-id="9725e-158">É claro que você também pode criar e executar os programas de Q# na linha de comando, simplesmente instalando o SDK do .NET Core e os modelos de projeto do QDK.</span><span class="sxs-lookup"><span data-stu-id="9725e-158">Of course, you can also build and run Q# programs from the command line by simply installing the .NET Core SDK and the QDK project templates.</span></span> 

1. <span data-ttu-id="9725e-159">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9725e-159">Pre-requisites</span></span>

    - [<span data-ttu-id="9725e-160">SDK do .NET Core 3,1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9725e-160">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="9725e-161">Instalar os modelos de projeto do Quantum para .NET</span><span class="sxs-lookup"><span data-stu-id="9725e-161">Install the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="9725e-162">Agora você tem o Quantum development kit instalado e pronto para uso em seus próprios aplicativos e suas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="9725e-162">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="9725e-163">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="9725e-163">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="9725e-164">Crie um novo aplicativo</span><span class="sxs-lookup"><span data-stu-id="9725e-164">Create a new application</span></span>

       ```dotnetcli
       dotnet new console -lang "Q#" -o runSayHello
       ```

    - <span data-ttu-id="9725e-165">Navegue até o diretório do novo aplicativo</span><span class="sxs-lookup"><span data-stu-id="9725e-165">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="9725e-166">Você deverá ver que dois arquivos foram criados, juntamente com os arquivos de projeto do aplicativo: um arquivo Q# (`Operation.qs`) e um arquivo de host C# (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="9725e-166">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="9725e-167">Executar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="9725e-167">Run the application</span></span>

        ```dotnetcli
        dotnet run
        ```

        <span data-ttu-id="9725e-168">Você deverá ver a seguinte saída: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="9725e-168">You should see the following output: `Hello quantum world!`</span></span>

    
## <a name="whats-next"></a><span data-ttu-id="9725e-169">O que vem a seguir?</span><span class="sxs-lookup"><span data-stu-id="9725e-169">What's next?</span></span>

<span data-ttu-id="9725e-170">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="9725e-170">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
