---
title: Saiba como atualizar o Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: ed2a90749bbe245dde97424fc3191682f995d85b
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819732"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="bec20-102">Atualizar o Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="bec20-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="bec20-103">Saiba como atualizar o Microsoft Quantum Development Kit (QDK) para a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="bec20-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="bec20-104">Este artigo pressupõe que você já tenha o QDK instalado.</span><span class="sxs-lookup"><span data-stu-id="bec20-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="bec20-105">Se você estiver instalando o pela primeira vez, consulte o guia de [instalação](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="bec20-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="bec20-106">É recomendável manter-se atualizado com a versão mais recente do QDK.</span><span class="sxs-lookup"><span data-stu-id="bec20-106">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="bec20-107">Siga este guia de atualização para atualizar para a versão mais recente do QDK.</span><span class="sxs-lookup"><span data-stu-id="bec20-107">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="bec20-108">O processo consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="bec20-108">The process consists of two parts:</span></span>
1. <span data-ttu-id="bec20-109">Atualizando seus arquivos e projetos do Q # existentes para alinhar seu código com qualquer sintaxe atualizada</span><span class="sxs-lookup"><span data-stu-id="bec20-109">updating your existing Q# files and projects to align your code with any updated syntax</span></span>
2. <span data-ttu-id="bec20-110">Atualizando o próprio QDK para seu ambiente de desenvolvimento escolhido</span><span class="sxs-lookup"><span data-stu-id="bec20-110">updating the QDK itself for your chosen development environment</span></span> 

## <a name="updating-q-projects"></a><span data-ttu-id="bec20-111">Atualizando projetos de Q #</span><span class="sxs-lookup"><span data-stu-id="bec20-111">Updating Q# Projects</span></span> 

<span data-ttu-id="bec20-112">Independentemente de você estar usando C# ou Python para hospedar operações Q #, siga estas instruções para atualizar seus projetos do q #.</span><span class="sxs-lookup"><span data-stu-id="bec20-112">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="bec20-113">Primeiro, verifique se você tem a versão mais recente do [SDK do .NET Core 3,1](https://dotnet.microsoft.com/download).</span><span class="sxs-lookup"><span data-stu-id="bec20-113">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="bec20-114">Execute o seguinte comando no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="bec20-114">Run the following command in the command prompt:</span></span>
    ```bash
    dotnet --version
    ```
<span data-ttu-id="bec20-115">Verifique se a saída é `3.1.100` ou superior.</span><span class="sxs-lookup"><span data-stu-id="bec20-115">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="bec20-116">Caso contrário, instale a [versão mais recente](https://dotnet.microsoft.com/download) e verifique novamente.</span><span class="sxs-lookup"><span data-stu-id="bec20-116">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="bec20-117">Em seguida, siga as instruções abaixo, dependendo da sua configuração (Visual Studio, Visual Studio Code ou diretamente a linha de comando).</span><span class="sxs-lookup"><span data-stu-id="bec20-117">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="bec20-118">Atualizar projetos do Q # no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bec20-118">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="bec20-119">Atualize para a versão mais recente do Visual Studio 2019, consulte [aqui](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) para obter instruções</span><span class="sxs-lookup"><span data-stu-id="bec20-119">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
2. <span data-ttu-id="bec20-120">Abra sua solução no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bec20-120">Open your solution in Visual Studio</span></span>
3. <span data-ttu-id="bec20-121">No menu, selecione **criar** -> **solução de limpeza**</span><span class="sxs-lookup"><span data-stu-id="bec20-121">From the menu, select **Build** -> **Clean Solution**</span></span>
4. <span data-ttu-id="bec20-122">Em cada um dos seus arquivos. csproj, atualize a estrutura de destino para `netcoreapp3.0` (ou `netstandard2.1` se for um projeto de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="bec20-122">In each of your .csproj files, update the target framework to `netcoreapp3.0` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="bec20-123">Ou seja, edite as linhas do formulário:</span><span class="sxs-lookup"><span data-stu-id="bec20-123">That is, edit lines of the form:</span></span>
    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```
    <span data-ttu-id="bec20-124">Você pode encontrar mais detalhes sobre como especificar estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="bec20-124">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
5. <span data-ttu-id="bec20-125">Salvar e fechar todos os arquivos em sua solução</span><span class="sxs-lookup"><span data-stu-id="bec20-125">Save and close all files in your solution</span></span>
6. <span data-ttu-id="bec20-126">Selecione **ferramentas** ->  -> de **linha de comando** **prompt de comando do desenvolvedor**</span><span class="sxs-lookup"><span data-stu-id="bec20-126">Select **Tools** -> **Command Line** -> **Developer Command Prompt**</span></span>
7. <span data-ttu-id="bec20-127">Para cada projeto na solução, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="bec20-127">For each project in the solution, run the following command:</span></span>
    ```bash
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```
    <span data-ttu-id="bec20-128">Se seus projetos usarem qualquer outro pacote do Microsoft. Quantum (por exemplo, Microsoft. Quantum. Numerics), execute o comando para eles também.</span><span class="sxs-lookup"><span data-stu-id="bec20-128">If your projects use any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
8. <span data-ttu-id="bec20-129">Feche o prompt de comando e selecione **compilar** -> **Compilar solução** ( *não selecione* recompilar solução, pois a recompilação falhará inicialmente)</span><span class="sxs-lookup"><span data-stu-id="bec20-129">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution, as rebuilding will initially fail)</span></span>

<span data-ttu-id="bec20-130">Agora você pode pular para [atualizar sua extensão QDK do Visual Studio](#update-visual-studio-qdk-extension).</span><span class="sxs-lookup"><span data-stu-id="bec20-130">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="bec20-131">Atualizar projetos do Q # no Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="bec20-131">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="bec20-132">Em Visual Studio Code, abra a pasta que contém o projeto a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="bec20-132">In Visual Studio Code, open the folder containing the project to update</span></span>
2. <span data-ttu-id="bec20-133">Selecionar **terminal** -> **novo terminal**</span><span class="sxs-lookup"><span data-stu-id="bec20-133">Select **Terminal** -> **New Terminal**</span></span>
3. <span data-ttu-id="bec20-134">Siga as instruções para atualizar usando a linha de comando (diretamente abaixo)</span><span class="sxs-lookup"><span data-stu-id="bec20-134">Follow the instructions for updating using the command line (directly below)</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="bec20-135">Atualizar projetos do Q # usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="bec20-135">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="bec20-136">Navegue até a pasta que contém o arquivo de projeto</span><span class="sxs-lookup"><span data-stu-id="bec20-136">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="bec20-137">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="bec20-137">Run the following command:</span></span>
    ```bash
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="bec20-138">Em cada um dos seus arquivos. csproj, atualize a estrutura de destino para `netcoreapp3.0` (ou `netstandard2.1` se for um projeto de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="bec20-138">In each of your .csproj files, update the target framework to `netcoreapp3.0` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="bec20-139">Ou seja, edite as linhas do formulário:</span><span class="sxs-lookup"><span data-stu-id="bec20-139">That is, edit lines of the form:</span></span>
    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```
    <span data-ttu-id="bec20-140">Você pode encontrar mais detalhes sobre como especificar estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="bec20-140">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
4. <span data-ttu-id="bec20-141">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="bec20-141">Run the following command:</span></span>
    ```bash
    dotnet add package Microsoft.Quantum.Development.Kit
    ```
    <span data-ttu-id="bec20-142">Se seu projeto usar qualquer outro pacote do Microsoft. Quantum (por exemplo, Microsoft. Quantum. Numerics), execute o comando para eles também.</span><span class="sxs-lookup"><span data-stu-id="bec20-142">If your project uses any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
5. <span data-ttu-id="bec20-143">Salve e feche todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="bec20-143">Save and close all files.</span></span>
6. <span data-ttu-id="bec20-144">Repita a 1-4 para cada dependência do projeto e, em seguida, navegue de volta para a pasta que contém o projeto principal e execute:</span><span class="sxs-lookup"><span data-stu-id="bec20-144">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>
    ```bash
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="bec20-145">Com seus projetos do Q # agora atualizados, siga as instruções abaixo para atualizar o próprio QDK.</span><span class="sxs-lookup"><span data-stu-id="bec20-145">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="bec20-146">Atualizando o QDK</span><span class="sxs-lookup"><span data-stu-id="bec20-146">Updating the QDK</span></span>

<span data-ttu-id="bec20-147">O processo para atualizar o QDK varia de acordo com o ambiente e a linguagem de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="bec20-147">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="bec20-148">Selecione seu ambiente de desenvolvimento abaixo.</span><span class="sxs-lookup"><span data-stu-id="bec20-148">Select your development environment below.</span></span>

* [<span data-ttu-id="bec20-149">Python: atualizar a extensão IQ #</span><span class="sxs-lookup"><span data-stu-id="bec20-149">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="bec20-150">Blocos de anotações do Jupyter: Atualize a extensão IQ #</span><span class="sxs-lookup"><span data-stu-id="bec20-150">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="bec20-151">Visual Studio: atualizar a extensão QDK</span><span class="sxs-lookup"><span data-stu-id="bec20-151">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="bec20-152">VS Code: atualizar a extensão QDK</span><span class="sxs-lookup"><span data-stu-id="bec20-152">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="bec20-153">Linha de comando e C#: atualizar modelos de projeto</span><span class="sxs-lookup"><span data-stu-id="bec20-153">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="bec20-154">Atualizar IQ # para Python</span><span class="sxs-lookup"><span data-stu-id="bec20-154">Update IQ# for Python</span></span>

1. <span data-ttu-id="bec20-155">Atualizar o kernel `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="bec20-155">Update the `iqsharp` kernel</span></span> 

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="bec20-156">Verificar a versão do `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="bec20-156">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="bec20-157">Você deve ver o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="bec20-157">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```
    <span data-ttu-id="bec20-158">Não se preocupe se sua versão de `iqsharp` for maior, ela deverá corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="bec20-158">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="bec20-159">Atualizar o pacote de `qsharp`</span><span class="sxs-lookup"><span data-stu-id="bec20-159">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="bec20-160">Verificar a versão do `qsharp`</span><span class="sxs-lookup"><span data-stu-id="bec20-160">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="bec20-161">Você deve ver o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="bec20-161">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
5. <span data-ttu-id="bec20-162">Execute o seguinte comando no local de seus arquivos de `.qs`</span><span class="sxs-lookup"><span data-stu-id="bec20-162">Run the following command from the location of your `.qs` files</span></span>
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="bec20-163">Agora você pode usar a versão atualizada do QDK para executar seus programas de Quantum existentes.</span><span class="sxs-lookup"><span data-stu-id="bec20-163">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="bec20-164">Atualizar IQ # para notebooks Jupyter</span><span class="sxs-lookup"><span data-stu-id="bec20-164">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="bec20-165">Atualizar o kernel `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="bec20-165">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="bec20-166">Verificar a versão do `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="bec20-166">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="bec20-167">A saída deve ser semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="bec20-167">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```
    <span data-ttu-id="bec20-168">Não se preocupe se sua versão de `iqsharp` for maior, ela deverá corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="bec20-168">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="bec20-169">Execute o seguinte comando de uma célula no seu Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="bec20-169">Run the following command from a cell in your Jupyter Notebook:</span></span>
    ```
    %workspace reload
    ```

4. <span data-ttu-id="bec20-170">Agora você pode abrir um bloco de anotações do Jupyter existente e executá-lo com o QDK atualizado.</span><span class="sxs-lookup"><span data-stu-id="bec20-170">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="bec20-171">Atualizar a extensão QDK do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bec20-171">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="bec20-172">Atualizar a extensão do Q # Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bec20-172">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="bec20-173">O Visual Studio solicita que você aceite atualizações para a [extensão Quantum do Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="bec20-173">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="bec20-174">Aceitar a atualização</span><span class="sxs-lookup"><span data-stu-id="bec20-174">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="bec20-175">Os modelos de projeto são atualizados com a extensão.</span><span class="sxs-lookup"><span data-stu-id="bec20-175">The project templates are updated with the extension.</span></span> <span data-ttu-id="bec20-176">Os modelos atualizados se aplicam apenas a projetos recém-criados.</span><span class="sxs-lookup"><span data-stu-id="bec20-176">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="bec20-177">O código para seus projetos existentes não é atualizado quando a extensão é atualizada.</span><span class="sxs-lookup"><span data-stu-id="bec20-177">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="bec20-178">Atualizar VS Code extensão QDK</span><span class="sxs-lookup"><span data-stu-id="bec20-178">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="bec20-179">Atualizar a extensão de VS Code Quantum</span><span class="sxs-lookup"><span data-stu-id="bec20-179">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="bec20-180">Reiniciar VS Code</span><span class="sxs-lookup"><span data-stu-id="bec20-180">Restart VS Code</span></span>
    - <span data-ttu-id="bec20-181">Navegue até a guia **extensões**</span><span class="sxs-lookup"><span data-stu-id="bec20-181">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="bec20-182">Selecione o **Microsoft Quantum Development Kit para Visual Studio Code** extensão</span><span class="sxs-lookup"><span data-stu-id="bec20-182">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="bec20-183">Recarregar a extensão</span><span class="sxs-lookup"><span data-stu-id="bec20-183">Reload the extension</span></span>

2. <span data-ttu-id="bec20-184">Atualize os modelos de projeto Quantum:</span><span class="sxs-lookup"><span data-stu-id="bec20-184">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="bec20-185">Acesse **Exibir** -> **Paleta de Comandos**</span><span class="sxs-lookup"><span data-stu-id="bec20-185">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="bec20-186">Selecione **Q #: instalar modelos de projeto**</span><span class="sxs-lookup"><span data-stu-id="bec20-186">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="bec20-187">Após alguns segundos, você deve obter um pop-up confirmando "modelos de projeto instalados com êxito"</span><span class="sxs-lookup"><span data-stu-id="bec20-187">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="bec20-188">C#, usando a ferramenta de linha de comando `dotnet`</span><span class="sxs-lookup"><span data-stu-id="bec20-188">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="bec20-189">Atualizar os modelos de projeto Quantum para .NET</span><span class="sxs-lookup"><span data-stu-id="bec20-189">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a><span data-ttu-id="bec20-190">O que vem a seguir?</span><span class="sxs-lookup"><span data-stu-id="bec20-190">What's next?</span></span>

<span data-ttu-id="bec20-191">Agora que você atualizou o kit de desenvolvimento Quantum em seu ambiente preferido, você pode continuar a desenvolver e executar seus programas Quantum.</span><span class="sxs-lookup"><span data-stu-id="bec20-191">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="bec20-192">Se você ainda não escreveu um programa, você pode começar com [seu primeiro programa Quantum](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="bec20-192">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
