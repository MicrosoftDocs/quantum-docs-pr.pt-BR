---
title: 'Saiba como criar um projeto do Q # com o kit de desenvolvimento Quantum (QDK)'
description: 'Inicialize um projeto para o desenvolvimento Quantum com o QDK e o Q # no ambiente de desenvolvimento de sua escolha'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: 8af8e3288aab731520ede984d5f89644de292385
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84578204"
---
# <a name="create-a-q-project-in-your-development-environment"></a><span data-ttu-id="07d46-103">Criar um projeto do Q # em seu ambiente de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="07d46-103">Create a Q# project in your development environment</span></span>

<span data-ttu-id="07d46-104">Saiba como criar um projeto do Q # com o QDK.</span><span class="sxs-lookup"><span data-stu-id="07d46-104">Learn how to create a Q# project with the QDK.</span></span>

<span data-ttu-id="07d46-105">Um projeto Q # contém os arquivos Q # contendo o código Quantum, bem como um programa de host para executar o programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="07d46-105">A Q# project contains Q# files containing quantum code, as well as a host program to run the quantum program.</span></span> <span data-ttu-id="07d46-106">Você pode escrever o programa host em linguagens .NET, como C#, ou em Python.</span><span class="sxs-lookup"><span data-stu-id="07d46-106">You can write the host program in .NET languages such as C#, or in Python.</span></span> <span data-ttu-id="07d46-107">Você também pode executar o código Q # em um Jupyter Notebook usando o kernel IQ #.</span><span class="sxs-lookup"><span data-stu-id="07d46-107">You can also run Q# code in a Jupyter Notebook using the IQ# kernel.</span></span>

<span data-ttu-id="07d46-108">Escolha seu ambiente de desenvolvimento e idioma nas seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="07d46-108">Choose your development environment and language from the sections below:</span></span>

* [<span data-ttu-id="07d46-109">Python</span><span class="sxs-lookup"><span data-stu-id="07d46-109">Python</span></span>](#create-a-python-project)
* [<span data-ttu-id="07d46-110">Jupyter Notebooks do Q#</span><span class="sxs-lookup"><span data-stu-id="07d46-110">Q# Jupyter Notebooks</span></span>](#create-a-q-jupyter-notebook-project)
* [<span data-ttu-id="07d46-111">C# com Visual Studio</span><span class="sxs-lookup"><span data-stu-id="07d46-111">C# with Visual Studio</span></span>](#create-a-c-project-on-windows-using-visual-studio)
* [<span data-ttu-id="07d46-112">C# com VS Code</span><span class="sxs-lookup"><span data-stu-id="07d46-112">C# with VS Code</span></span>](#create-a-c-project-using-vs-code)
* [<span data-ttu-id="07d46-113">C# com a linha de comando</span><span class="sxs-lookup"><span data-stu-id="07d46-113">C# with the command line</span></span>](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a><span data-ttu-id="07d46-114">Criar um projeto do Python</span><span class="sxs-lookup"><span data-stu-id="07d46-114">Create a Python project</span></span>

1. <span data-ttu-id="07d46-115">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="07d46-115">Pre-requisites</span></span>

     * <span data-ttu-id="07d46-116">Instalar o [Kit de desenvolvimento Quantum para Python](xref:microsoft.quantum.install.python)</span><span class="sxs-lookup"><span data-stu-id="07d46-116">Install the [Quantum Development Kit for Python](xref:microsoft.quantum.install.python)</span></span>

1. <span data-ttu-id="07d46-117">Criar uma pasta para seu projeto e navegar até essa pasta</span><span class="sxs-lookup"><span data-stu-id="07d46-117">Create a folder for your project, and navigate to that folder</span></span>

1. <span data-ttu-id="07d46-118">Crie um arquivo Q # chamado `Operation.qs` e adicione o código q # a ele.</span><span class="sxs-lookup"><span data-stu-id="07d46-118">Create a Q# file called `Operation.qs`, and add your Q# code to it.</span></span> <span data-ttu-id="07d46-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="07d46-119">For example:</span></span>

    ```qsharp
    namespace HelloWorld {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation SayHello() : Result {
            Message("Hello from quantum world!");
            return Zero;
        }
    }
    ```

1. <span data-ttu-id="07d46-120">Crie um arquivo de host Python chamado `host.py` para chamar a operação Q #.</span><span class="sxs-lookup"><span data-stu-id="07d46-120">Create a python host file called `host.py` to call your Q# operation.</span></span> <span data-ttu-id="07d46-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="07d46-121">For example:</span></span>

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. <span data-ttu-id="07d46-122">Execute o programa:</span><span class="sxs-lookup"><span data-stu-id="07d46-122">Run the program:</span></span>

    ```
    python host.py
    ```

1. <span data-ttu-id="07d46-123">Verifique a saída.</span><span class="sxs-lookup"><span data-stu-id="07d46-123">Verify the output.</span></span> <span data-ttu-id="07d46-124">Seu programa deverá gerar as seguintes linhas:</span><span class="sxs-lookup"><span data-stu-id="07d46-124">Your program should output the following lines:</span></span>

    ```
    Hello from quantum world!
    0
    ```

<span data-ttu-id="07d46-125">Agora você pode continuar a desenvolver seu programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="07d46-125">You can now continue to develop your quantum program.</span></span>

## <a name="create-a-q-jupyter-notebook-project"></a><span data-ttu-id="07d46-126">Criar um projeto de Jupyter Notebook do Q #</span><span class="sxs-lookup"><span data-stu-id="07d46-126">Create a Q# Jupyter Notebook project</span></span>

1. <span data-ttu-id="07d46-127">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="07d46-127">Pre-requisites</span></span>

    * <span data-ttu-id="07d46-128">Instalar o [Kit de desenvolvimento Quantum para notebooks Jupyter](xref:microsoft.quantum.install.jupyter)</span><span class="sxs-lookup"><span data-stu-id="07d46-128">Install the [Quantum Development Kit for Jupyter Notebooks](xref:microsoft.quantum.install.jupyter)</span></span>

1. <span data-ttu-id="07d46-129">Execute o seguinte comando para iniciar o servidor de notebook:</span><span class="sxs-lookup"><span data-stu-id="07d46-129">Run the following command to start the notebook server:</span></span>

    ```
    jupyter notebook
    ```

1. <span data-ttu-id="07d46-130">Procure a URL mostrada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="07d46-130">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="07d46-131">Por exemplo: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span><span class="sxs-lookup"><span data-stu-id="07d46-131">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

1. <span data-ttu-id="07d46-132">Uma página Jupyter aparece no navegador.</span><span class="sxs-lookup"><span data-stu-id="07d46-132">A Jupyter page appears in the browser.</span></span> <span data-ttu-id="07d46-133">Na guia **arquivos** , selecione **novo**  >  **Q #** para criar um Jupyter notebook com um kernel Q #.</span><span class="sxs-lookup"><span data-stu-id="07d46-133">On the **Files** tab, select **New** > **Q#** to create a Jupyter Notebook with a Q# kernel.</span></span> <span data-ttu-id="07d46-134">Adicione o seguinte código à primeira célula do bloco de anotações:</span><span class="sxs-lookup"><span data-stu-id="07d46-134">Add the following code to the first notebook cell:</span></span>

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. <span data-ttu-id="07d46-135">Selecione **Cell**  >  **células de execução** de célula para executar o bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="07d46-135">Select **Cell** > **Run Cells** to run the notebook.</span></span> <span data-ttu-id="07d46-136">`SayHello`será exibido em breve na saída da célula:</span><span class="sxs-lookup"><span data-stu-id="07d46-136">`SayHello` will soon appear in the cell output:</span></span>

    ![Jupyter Notebook célula com código Q #](~/media/install-guide-jupyter.png)

    <span data-ttu-id="07d46-138">Ao executar em notebooks Jupyter, o código Q # é compilado e o notebook gera o nome da (s) operação (ões) que encontrará.</span><span class="sxs-lookup"><span data-stu-id="07d46-138">When running in Jupyter Notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>

1. <span data-ttu-id="07d46-139">Em uma nova célula, usando um computador quântico, simule a execução da operação que você acabou de criar usando a mágica `%simulate`:</span><span class="sxs-lookup"><span data-stu-id="07d46-139">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

    ![Jupyter Notebook célula com% simula mágica](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="07d46-141">Você deverá ver a mensagem impressa na tela, juntamente com o resultado da operação que você invocou (nesse caso, vazio).</span><span class="sxs-lookup"><span data-stu-id="07d46-141">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>

<span data-ttu-id="07d46-142">Agora você pode adicionar outras operações Q # para continuar o desenvolvimento do Quantum.</span><span class="sxs-lookup"><span data-stu-id="07d46-142">You can now add other Q# operations to continue your quantum development.</span></span>

## <a name="create-a-c-project-on-windows-using-visual-studio"></a><span data-ttu-id="07d46-143">Criar um projeto C# no Windows usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="07d46-143">Create a C# project on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="07d46-144">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="07d46-144">Pre-requisites</span></span>

    * <span data-ttu-id="07d46-145">Instalar a [extensão do kit de desenvolvimento do Quantum para Visual Studio](xref:microsoft.quantum.install.cs)</span><span class="sxs-lookup"><span data-stu-id="07d46-145">Install the [Quantum Development Kit extension for Visual Studio](xref:microsoft.quantum.install.cs)</span></span>

1. <span data-ttu-id="07d46-146">Criar um aplicativo Q#</span><span class="sxs-lookup"><span data-stu-id="07d46-146">Create a new Q# application</span></span>

    * <span data-ttu-id="07d46-147">Ir para **arquivo**  ->  **novo**  ->  **projeto**</span><span class="sxs-lookup"><span data-stu-id="07d46-147">Go to **File** -> **New** -> **Project**</span></span>
    * <span data-ttu-id="07d46-148">Digite `Q#` na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="07d46-148">Type `Q#` in the search box</span></span>
    * <span data-ttu-id="07d46-149">Selecione **Aplicativo Q#**</span><span class="sxs-lookup"><span data-stu-id="07d46-149">Select **Q# Application**</span></span>
    * <span data-ttu-id="07d46-150">Selecione **Avançar**</span><span class="sxs-lookup"><span data-stu-id="07d46-150">Select **Next**</span></span>
    * <span data-ttu-id="07d46-151">Escolha um nome e uma localização para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="07d46-151">Choose a name and location for your application</span></span>
    * <span data-ttu-id="07d46-152">Escolha **Criar**</span><span class="sxs-lookup"><span data-stu-id="07d46-152">Select **Create**</span></span>

1. <span data-ttu-id="07d46-153">Inspecionar o projeto</span><span class="sxs-lookup"><span data-stu-id="07d46-153">Inspect the project</span></span>

    <span data-ttu-id="07d46-154">Você deverá ver que dois arquivos foram criados: `Driver.cs`, que é o aplicativo host C#; e `Operation.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="07d46-154">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

1. <span data-ttu-id="07d46-155">Execute o aplicativo</span><span class="sxs-lookup"><span data-stu-id="07d46-155">Run the application</span></span>

    * <span data-ttu-id="07d46-156">Selecione **depurar**  ->  **Iniciar sem depuração**</span><span class="sxs-lookup"><span data-stu-id="07d46-156">Select **Debug** -> **Start Without Debugging**</span></span>
    * <span data-ttu-id="07d46-157">Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.</span><span class="sxs-lookup"><span data-stu-id="07d46-157">You should see the text `Hello quantum world!` printed to a console window.</span></span>

<span data-ttu-id="07d46-158">Agora você pode continuar o desenvolvimento do Quantum usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="07d46-158">You can now continue your quantum development using Visual Studio</span></span>

> [!NOTE]
> * <span data-ttu-id="07d46-159">Caso você tenha vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas.</span><span class="sxs-lookup"><span data-stu-id="07d46-159">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="create-a-c-project-using-vs-code"></a><span data-ttu-id="07d46-160">Criar um projeto C#, usando VS Code</span><span class="sxs-lookup"><span data-stu-id="07d46-160">Create a C# project, using VS Code</span></span>

1. <span data-ttu-id="07d46-161">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="07d46-161">Pre-requisites</span></span>

    * <span data-ttu-id="07d46-162">Instalar a [extensão do kit de desenvolvimento Quantum para vs Code](xref:microsoft.quantum.install.cs)</span><span class="sxs-lookup"><span data-stu-id="07d46-162">Install the [Quantum Development Kit extension for VS Code](xref:microsoft.quantum.install.cs)</span></span>

1. <span data-ttu-id="07d46-163">Crie um novo projeto:</span><span class="sxs-lookup"><span data-stu-id="07d46-163">Create a new project:</span></span>

    * <span data-ttu-id="07d46-164">Ir para **Exibir**  ->  **paleta de comandos**</span><span class="sxs-lookup"><span data-stu-id="07d46-164">Go to **View** -> **Command Palette**</span></span>
    * <span data-ttu-id="07d46-165">Selecione **Q #: criar novo projeto**</span><span class="sxs-lookup"><span data-stu-id="07d46-165">Select **Q#: Create New Project**</span></span>
    * <span data-ttu-id="07d46-166">Selecionar **aplicativo de console autônomo**</span><span class="sxs-lookup"><span data-stu-id="07d46-166">Select **Standalone console application**</span></span>
    * <span data-ttu-id="07d46-167">Navegue até a localização no sistema de arquivos em que deseja criar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="07d46-167">Navigate to the location on the file system where you would like to create the application</span></span>
    * <span data-ttu-id="07d46-168">Clique no botão **Abrir novo projeto...** após a criação do projeto</span><span class="sxs-lookup"><span data-stu-id="07d46-168">Click on the **Open new project...** button, once the project has been created</span></span>

1. <span data-ttu-id="07d46-169">Executar o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="07d46-169">Run the application:</span></span>

    * <span data-ttu-id="07d46-170">Ir para **terminal**  ->  **novo terminal**</span><span class="sxs-lookup"><span data-stu-id="07d46-170">Go to **Terminal** -> **New Terminal**</span></span>
    * <span data-ttu-id="07d46-171">Inserir `dotnet run`</span><span class="sxs-lookup"><span data-stu-id="07d46-171">Enter `dotnet run`</span></span>
    * <span data-ttu-id="07d46-172">Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="07d46-172">You should see the following text in the output window `Hello quantum world!`</span></span>

<span data-ttu-id="07d46-173">Agora você pode continuar o desenvolvimento do Quantum usando Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="07d46-173">You can now continue your quantum development using Visual Studio Code.</span></span>

> [!NOTE]
> * <span data-ttu-id="07d46-174">No momento, não há suporte para workspaces com várias pastas raiz na extensão do Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="07d46-174">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="07d46-175">Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="07d46-175">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a><span data-ttu-id="07d46-176">Criar um projeto C# usando a `dotnet` ferramenta de linha de comando</span><span class="sxs-lookup"><span data-stu-id="07d46-176">Create a C# project, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="07d46-177">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="07d46-177">Pre-requisites</span></span>

    * <span data-ttu-id="07d46-178">Instalar o [Kit de desenvolvimento Quantum para a linha de comando](xref:microsoft.quantum.install.standalone)</span><span class="sxs-lookup"><span data-stu-id="07d46-178">Install the [Quantum Development Kit for the command line](xref:microsoft.quantum.install.standalone)</span></span>

1. <span data-ttu-id="07d46-179">Crie um novo aplicativo</span><span class="sxs-lookup"><span data-stu-id="07d46-179">Create a new application</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o <project name>
    ```

1. <span data-ttu-id="07d46-180">Navegue até o diretório do novo aplicativo</span><span class="sxs-lookup"><span data-stu-id="07d46-180">Navigate to the new application directory</span></span>

    ```
    cd <project name>
    ```

    <span data-ttu-id="07d46-181">Você deverá ver que dois arquivos foram criados, juntamente com os arquivos de projeto do aplicativo: um arquivo Q# (`Operation.qs`) e um arquivo de host C# (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="07d46-181">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

1. <span data-ttu-id="07d46-182">Execute o aplicativo</span><span class="sxs-lookup"><span data-stu-id="07d46-182">Run the application</span></span>

    ```dotnetcli
    dotnet run
    ```

    <span data-ttu-id="07d46-183">Você deverá ver a seguinte saída: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="07d46-183">You should see the following output: `Hello quantum world!`</span></span>

<span data-ttu-id="07d46-184">Agora você continua o desenvolvimento do Quantum, usando as ferramentas de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="07d46-184">You now continue your quantum development, using command line tools.</span></span>

## <a name="next-steps"></a><span data-ttu-id="07d46-185">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="07d46-185">Next steps</span></span>

<span data-ttu-id="07d46-186">Agora que você criou um projeto em seu ambiente preferido, você pode continuar o desenvolvimento do Quantum.</span><span class="sxs-lookup"><span data-stu-id="07d46-186">Now that you have created a project in your preferred environment, you can continue your quantum development.</span></span>
