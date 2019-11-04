---
title: Saiba como instalar o QDK (Microsoft Quantum development kit)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 2a098d89f13278d7137bf182a184a74afb9393be
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462876"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="4e96a-102">Instalar o QDK (Microsoft Quantum development kit)</span><span class="sxs-lookup"><span data-stu-id="4e96a-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="4e96a-103">Saiba como instalar o QDK (Microsoft Quantum development kit) para começar a usar a programação quântica.</span><span class="sxs-lookup"><span data-stu-id="4e96a-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="4e96a-104">O QDK consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="4e96a-104">The QDK consists of:</span></span>

- <span data-ttu-id="4e96a-105">a linguagem de programação Q#</span><span class="sxs-lookup"><span data-stu-id="4e96a-105">the Q# programming language</span></span>
- <span data-ttu-id="4e96a-106">um conjunto de bibliotecas que abstrai a funcionalidade complexa no Q#</span><span class="sxs-lookup"><span data-stu-id="4e96a-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="4e96a-107">um aplicativo host (escrito em Python ou uma linguagem .NET) que executa operações quânticas escritas em Q#</span><span class="sxs-lookup"><span data-stu-id="4e96a-107">a host application (written in Python or a .NET language) that runs quantum operations written in Q#</span></span>
- <span data-ttu-id="4e96a-108">ferramentas para facilitar seu desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="4e96a-108">tools to facilitate your development</span></span>

<span data-ttu-id="4e96a-109">Dependendo do ambiente de desenvolvimento escolhido, há diferentes etapas de instalação.</span><span class="sxs-lookup"><span data-stu-id="4e96a-109">Depending on your chosen development environment, there are different installation steps.</span></span> <span data-ttu-id="4e96a-110">Escolha seu ambiente nas seções abaixo.</span><span class="sxs-lookup"><span data-stu-id="4e96a-110">Choose your environment from the sections below.</span></span>

## <a name="develop-with-python"></a><span data-ttu-id="4e96a-111">Desenvolvimento com o Python</span><span class="sxs-lookup"><span data-stu-id="4e96a-111">Develop with Python</span></span>

<span data-ttu-id="4e96a-112">O pacote qsharp para Python facilita a simulação de operações e funções de Q# no Python.</span><span class="sxs-lookup"><span data-stu-id="4e96a-112">The qsharp package for Python makes it easy to simulate Q# operations and functions from within Python.</span></span> <span data-ttu-id="4e96a-113">IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python que fornece a funcionalidade principal para compilar e simular operações Q#.</span><span class="sxs-lookup"><span data-stu-id="4e96a-113">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python that provides the core functionality for compiling and simulating Q# operations.</span></span>

1. <span data-ttu-id="4e96a-114">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4e96a-114">Pre-requisites</span></span>

    - <span data-ttu-id="4e96a-115">[Python](https://www.python.org/downloads/) 3.6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4e96a-115">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="4e96a-116">O gerenciador de pacotes Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="4e96a-116">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="4e96a-117">SDK do .NET Core 3.0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4e96a-117">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="4e96a-118">Instalar o pacote `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="4e96a-118">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="4e96a-119">Instalar o pacote `qsharp`</span><span class="sxs-lookup"><span data-stu-id="4e96a-119">Install the `qsharp` package</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="4e96a-120">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="4e96a-120">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="4e96a-121">Crie uma operação Q# mínima criando um arquivo chamado `Operation.qs` e adicionando o seguinte código a ele:</span><span class="sxs-lookup"><span data-stu-id="4e96a-121">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld
        {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Result {
                Message("Hello from quantum world!");
                return Zero;
            }
        }
        ```

    - <span data-ttu-id="4e96a-122">Crie um programa Python chamado `hello_world.py` para chamar a operação Q# `SayHello()`:</span><span class="sxs-lookup"><span data-stu-id="4e96a-122">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="4e96a-123">Execute o programa:</span><span class="sxs-lookup"><span data-stu-id="4e96a-123">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="4e96a-124">Verifique a saída.</span><span class="sxs-lookup"><span data-stu-id="4e96a-124">Verify the output.</span></span> <span data-ttu-id="4e96a-125">Seu programa deverá gerar as seguintes linhas:</span><span class="sxs-lookup"><span data-stu-id="4e96a-125">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a><span data-ttu-id="4e96a-126">Desenvolvimento com Jupyter notebooks</span><span class="sxs-lookup"><span data-stu-id="4e96a-126">Develop with Jupyter notebooks</span></span>

<span data-ttu-id="4e96a-127">Favoritos de configurações acadêmicas, laboratórios científicos e programação colaborativa baseada em uso online, os Jupyter Notebooks oferecem execução de código in-loco — agora incluindo código Q# — juntamente com instruções, anotações e outros conteúdos.</span><span class="sxs-lookup"><span data-stu-id="4e96a-127">A favorite of academic settings, scientific labs, and online-based collaborative programming, Jupyter Notebooks offer in-place code execution—now including Q# code—along with instructions, notes, and other content.</span></span>  <span data-ttu-id="4e96a-128">Aqui está o que você precisa fazer para começar a criar seus próprios notebooks de Q#.</span><span class="sxs-lookup"><span data-stu-id="4e96a-128">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="4e96a-129">IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade principal para compilar e simular operações Q#.</span><span class="sxs-lookup"><span data-stu-id="4e96a-129">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>


1. <span data-ttu-id="4e96a-130">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4e96a-130">Pre-requisites</span></span>

    - <span data-ttu-id="4e96a-131">[Python](https://www.python.org/downloads/) 3.6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4e96a-131">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="4e96a-132">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="4e96a-132">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="4e96a-133">SDK do .NET Core 3.0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4e96a-133">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="4e96a-134">Instalar o pacote `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="4e96a-134">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="4e96a-135">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="4e96a-135">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="4e96a-136">Execute o seguinte comando para iniciar o servidor de notebook:</span><span class="sxs-lookup"><span data-stu-id="4e96a-136">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="4e96a-137">Procure a URL mostrada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4e96a-137">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="4e96a-138">Por exemplo: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="4e96a-138">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

    - <span data-ttu-id="4e96a-139">Crie um Jupyter Notebook com um kernel do Q# e adicione o seguinte código à primeira célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="4e96a-139">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="4e96a-140">Execute esta célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="4e96a-140">Run this cell of the notebook:</span></span>

        ![Célula do Jupyter Notebook com código Q#](~/media/install-guide-jupyter.png)

        <span data-ttu-id="4e96a-142">Você deverá ver `SayHello` na saída da célula.</span><span class="sxs-lookup"><span data-stu-id="4e96a-142">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="4e96a-143">Durante a execução em Jupyter notebooks, o código Q# é compilado e o notebook gera o nome das operações encontradas.</span><span class="sxs-lookup"><span data-stu-id="4e96a-143">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="4e96a-144">Em uma nova célula, usando um computador quântico, simule a execução da operação que você acabou de criar usando a mágica `%simulate`:</span><span class="sxs-lookup"><span data-stu-id="4e96a-144">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

        ![Célula do Jupyter Notebook com a mágica %simulate](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="4e96a-146">Você deverá ver a mensagem impressa na tela, juntamente com o resultado da operação que você invocou (nesse caso, vazio).</span><span class="sxs-lookup"><span data-stu-id="4e96a-146">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>


## <a name="develop-with-c-on-windows-using-visual-studio"></a><span data-ttu-id="4e96a-147">Desenvolvimento com o C# no Windows usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4e96a-147">Develop with C# on Windows, using Visual Studio</span></span>

<span data-ttu-id="4e96a-148">O Visual Studio oferece um ambiente avançado para o desenvolvimento de programas de Q#, oferecendo ótimos recursos como conclusão de código e realce de sintaxe que orienta o desenvolvedor na criação de seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4e96a-148">Visual Studio offers a rich environment for developing Q# programs, offering great features like code completion and syntax highlighting that guide the developer in building their applications.</span></span>  <span data-ttu-id="4e96a-149">A extensão do Visual Studio para Q# contém modelos para arquivos e projetos do Q#, bem como realce de sintaxe e suporte para IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="4e96a-149">The Q# Visual Studio extension contains templates for Q# files and projects as well as syntax highlighting and IntelliSense support.</span></span>


1. <span data-ttu-id="4e96a-150">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4e96a-150">Pre-requisites</span></span>

    - <span data-ttu-id="4e96a-151">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, com a carga de trabalho de desenvolvimento multiplataforma com .NET Core habilitada</span><span class="sxs-lookup"><span data-stu-id="4e96a-151">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="4e96a-152">Instalar a extensão do Visual Studio para Q#</span><span class="sxs-lookup"><span data-stu-id="4e96a-152">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="4e96a-153">Baixar a [extensão do Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="4e96a-153">Download the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="4e96a-154">Adicionar a extensão ao Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4e96a-154">Add the extension to Visual Studio</span></span>

1. <span data-ttu-id="4e96a-155">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="4e96a-155">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="4e96a-156">Criar um aplicativo Q#</span><span class="sxs-lookup"><span data-stu-id="4e96a-156">Create a new Q# application</span></span>

        - <span data-ttu-id="4e96a-157">Acesse **Arquivo** -> **Novo** -> **Projeto**</span><span class="sxs-lookup"><span data-stu-id="4e96a-157">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="4e96a-158">Digite `Q#` na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="4e96a-158">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="4e96a-159">Selecione **Aplicativo Q#**</span><span class="sxs-lookup"><span data-stu-id="4e96a-159">Select **Q# Application**</span></span>
        - <span data-ttu-id="4e96a-160">Selecione **Avançar**</span><span class="sxs-lookup"><span data-stu-id="4e96a-160">Select **Next**</span></span>
        - <span data-ttu-id="4e96a-161">Escolha um nome e uma localização para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="4e96a-161">Choose a name and location for your application</span></span>
        - <span data-ttu-id="4e96a-162">Escolha **Criar**</span><span class="sxs-lookup"><span data-stu-id="4e96a-162">Select **Create**</span></span>

    - <span data-ttu-id="4e96a-163">Inspecionar o projeto</span><span class="sxs-lookup"><span data-stu-id="4e96a-163">Inspect the project</span></span>

        <span data-ttu-id="4e96a-164">Você deverá ver que dois arquivos foram criados: `Driver.cs`, que é o aplicativo host C#; e `Operation.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="4e96a-164">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="4e96a-165">Executar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="4e96a-165">Run the application</span></span>

        - <span data-ttu-id="4e96a-166">Selecione **Depurar** -> **Iniciar Sem Depuração**</span><span class="sxs-lookup"><span data-stu-id="4e96a-166">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="4e96a-167">Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.</span><span class="sxs-lookup"><span data-stu-id="4e96a-167">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="4e96a-168">Caso você tenha vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas.</span><span class="sxs-lookup"><span data-stu-id="4e96a-168">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="develop-with-c-using-visual-studio-code"></a><span data-ttu-id="4e96a-169">Desenvolver com C# usando o Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="4e96a-169">Develop with C#, using Visual Studio Code</span></span>

<span data-ttu-id="4e96a-170">O VS Code (Visual Studio Code) oferece um ambiente avançado para o desenvolvimento de programas de Q# entre vários ambientes de computadores, incluindo Windows, Linux e Mac e oferecendo ótimos recursos, tais como conclusão de código e realce de sintaxe, que orientam os desenvolvedores na criação dos respectivos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4e96a-170">Visual Studio Code (VS Code) offers a rich environment for developing Q# programs across many multiple computer environments, including Windows, Linux and Mac, offering great features like code completion and syntax highlighting that guide the developer in building their applications.</span></span>  <span data-ttu-id="4e96a-171">A extensão VS Code do Q# contém realce de sintaxe e trechos de código do Q#.</span><span class="sxs-lookup"><span data-stu-id="4e96a-171">The Q# VS Code extension contains syntax highlighting, and Q# code snippets.</span></span>

1. <span data-ttu-id="4e96a-172">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4e96a-172">Pre-requisites</span></span>

   - [<span data-ttu-id="4e96a-173">Código do VS</span><span class="sxs-lookup"><span data-stu-id="4e96a-173">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="4e96a-174">SDK do .NET Core 3.0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4e96a-174">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="4e96a-175">Instalar a extensão do VS Code para Quantum</span><span class="sxs-lookup"><span data-stu-id="4e96a-175">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="4e96a-176">Instalar a [extensão do VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span><span class="sxs-lookup"><span data-stu-id="4e96a-176">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="4e96a-177">Instale os modelos de projeto do Quantum:</span><span class="sxs-lookup"><span data-stu-id="4e96a-177">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="4e96a-178">Acesse **Exibir** -> **Paleta de Comandos**</span><span class="sxs-lookup"><span data-stu-id="4e96a-178">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="4e96a-179">Selecione **Q#: Instalar modelos de projeto**</span><span class="sxs-lookup"><span data-stu-id="4e96a-179">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="4e96a-180">Agora você tem o Quantum development kit instalado e pronto para uso em seus próprios aplicativos e suas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="4e96a-180">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="4e96a-181">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="4e96a-181">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="4e96a-182">Crie um novo projeto:</span><span class="sxs-lookup"><span data-stu-id="4e96a-182">Create a new project:</span></span>

        - <span data-ttu-id="4e96a-183">Acesse **Exibir** -> **Paleta de Comandos**</span><span class="sxs-lookup"><span data-stu-id="4e96a-183">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="4e96a-184">Selecione **Q#: Criar Projeto**</span><span class="sxs-lookup"><span data-stu-id="4e96a-184">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="4e96a-185">Navegue até a localização no sistema de arquivos em que deseja criar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="4e96a-185">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="4e96a-186">Clique no botão **Abrir novo projeto...** após a criação do projeto</span><span class="sxs-lookup"><span data-stu-id="4e96a-186">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="4e96a-187">Executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="4e96a-187">Run the application:</span></span>

        - <span data-ttu-id="4e96a-188">Acesse **Depurar** -> **Iniciar Sem Depuração**</span><span class="sxs-lookup"><span data-stu-id="4e96a-188">Go to **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="4e96a-189">Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="4e96a-189">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> * > * <span data-ttu-id="4e96a-190">No momento, não há suporte para workspaces com várias pastas raiz na extensão do Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="4e96a-190">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="4e96a-191">Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="4e96a-191">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="4e96a-192">Desenvolvimento com o C# usando a ferramenta de linha de comando `dotnet`</span><span class="sxs-lookup"><span data-stu-id="4e96a-192">Develop with C#, using the `dotnet` command-line tool</span></span>

<span data-ttu-id="4e96a-193">É claro que você também pode criar e executar os programas de Q# na linha de comando, simplesmente instalando o SDK do .NET Core e os modelos de projeto do QDK.</span><span class="sxs-lookup"><span data-stu-id="4e96a-193">Of course, you can also build and run Q# programs from the command line by simply installing the .NET Core SDK and the QDK project templates.</span></span> 

1. <span data-ttu-id="4e96a-194">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4e96a-194">Pre-requisites</span></span>

    - [<span data-ttu-id="4e96a-195">SDK do .NET Core 3.0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4e96a-195">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="4e96a-196">Instalar os modelos de projeto do Quantum para .NET</span><span class="sxs-lookup"><span data-stu-id="4e96a-196">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="4e96a-197">Agora você tem o Quantum development kit instalado e pronto para uso em seus próprios aplicativos e suas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="4e96a-197">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="4e96a-198">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="4e96a-198">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="4e96a-199">Crie um novo aplicativo</span><span class="sxs-lookup"><span data-stu-id="4e96a-199">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="4e96a-200">Navegue até o diretório do novo aplicativo</span><span class="sxs-lookup"><span data-stu-id="4e96a-200">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="4e96a-201">Você deverá ver que dois arquivos foram criados, juntamente com os arquivos de projeto do aplicativo: um arquivo Q# (`Operation.qs`) e um arquivo de host C# (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="4e96a-201">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="4e96a-202">Executar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="4e96a-202">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="4e96a-203">Você deverá ver a seguinte saída: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="4e96a-203">You should see the following output: `Hello quantum world!`</span></span>

## <a name="whats-next"></a><span data-ttu-id="4e96a-204">O que vem a seguir?</span><span class="sxs-lookup"><span data-stu-id="4e96a-204">What's next?</span></span>

<span data-ttu-id="4e96a-205">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="4e96a-205">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
