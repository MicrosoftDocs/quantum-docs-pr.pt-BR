---
title: Atualizar o kit de desenvolvimento Quantum (QDK)
description: 'Descreve como atualizar seus projetos do Q # e o Microsoft Quantum Development Kit para a versão atual.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 53f72f1d49ae32a5a8572a1cf68a66a1d9b45e4a
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426902"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="29b59-103">Atualizar o Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="29b59-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="29b59-104">Saiba como atualizar o Microsoft Quantum Development Kit (QDK) para a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="29b59-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="29b59-105">Este artigo pressupõe que você já tenha o QDK instalado.</span><span class="sxs-lookup"><span data-stu-id="29b59-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="29b59-106">Se você estiver instalando o pela primeira vez, consulte o guia de [instalação](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="29b59-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="29b59-107">É recomendável manter-se atualizado com a versão mais recente do QDK.</span><span class="sxs-lookup"><span data-stu-id="29b59-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="29b59-108">Siga este guia de atualização para atualizar para a versão mais recente do QDK.</span><span class="sxs-lookup"><span data-stu-id="29b59-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="29b59-109">O processo consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="29b59-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="29b59-110">Atualizando seus arquivos e projetos do Q # existentes para alinhar seu código com qualquer sintaxe atualizada</span><span class="sxs-lookup"><span data-stu-id="29b59-110">updating your existing Q# files and projects to align your code with any updated syntax</span></span>
2. <span data-ttu-id="29b59-111">Atualizando o próprio QDK para seu ambiente de desenvolvimento escolhido</span><span class="sxs-lookup"><span data-stu-id="29b59-111">updating the QDK itself for your chosen development environment</span></span> 

## <a name="updating-q-projects"></a><span data-ttu-id="29b59-112">Atualizando projetos de Q #</span><span class="sxs-lookup"><span data-stu-id="29b59-112">Updating Q# Projects</span></span> 

<span data-ttu-id="29b59-113">Independentemente de você estar usando C# ou Python para hospedar operações Q #, siga estas instruções para atualizar seus projetos do Q #.</span><span class="sxs-lookup"><span data-stu-id="29b59-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="29b59-114">Primeiro, verifique se você tem a versão mais recente do [SDK do .NET Core 3,1](https://dotnet.microsoft.com/download).</span><span class="sxs-lookup"><span data-stu-id="29b59-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="29b59-115">Execute o seguinte comando no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="29b59-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="29b59-116">Verifique se a saída é `3.1.100` ou mais alta.</span><span class="sxs-lookup"><span data-stu-id="29b59-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="29b59-117">Caso contrário, instale a [versão mais recente](https://dotnet.microsoft.com/download) e verifique novamente.</span><span class="sxs-lookup"><span data-stu-id="29b59-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="29b59-118">Em seguida, siga as instruções abaixo, dependendo da sua configuração (Visual Studio, Visual Studio Code ou diretamente a linha de comando).</span><span class="sxs-lookup"><span data-stu-id="29b59-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="29b59-119">Atualizar projetos do Q # no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="29b59-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="29b59-120">Atualize para a versão mais recente do Visual Studio 2019, consulte [aqui](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) para obter instruções</span><span class="sxs-lookup"><span data-stu-id="29b59-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
2. <span data-ttu-id="29b59-121">Abra sua solução no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="29b59-121">Open your solution in Visual Studio</span></span>
3. <span data-ttu-id="29b59-122">No menu, selecione **criar**  ->  **solução limpa**</span><span class="sxs-lookup"><span data-stu-id="29b59-122">From the menu, select **Build** -> **Clean Solution**</span></span>
4. <span data-ttu-id="29b59-123">Em cada um dos seus arquivos. csproj, atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se for um projeto de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="29b59-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="29b59-124">Ou seja, edite as linhas do formulário:</span><span class="sxs-lookup"><span data-stu-id="29b59-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="29b59-125">Você pode encontrar mais detalhes sobre como especificar estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="29b59-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
5. <span data-ttu-id="29b59-126">Salvar e fechar todos os arquivos em sua solução</span><span class="sxs-lookup"><span data-stu-id="29b59-126">Save and close all files in your solution</span></span>
6. <span data-ttu-id="29b59-127">Selecione **ferramentas**  ->  **linha de comando**  ->  **prompt de comando do desenvolvedor**</span><span class="sxs-lookup"><span data-stu-id="29b59-127">Select **Tools** -> **Command Line** -> **Developer Command Prompt**</span></span>
7. <span data-ttu-id="29b59-128">Para cada projeto na solução, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="29b59-128">For each project in the solution, run the following command:</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="29b59-129">Se seus projetos usarem qualquer outro pacote do Microsoft. Quantum (por exemplo, Microsoft. Quantum. Numerics), execute o comando para eles também.</span><span class="sxs-lookup"><span data-stu-id="29b59-129">If your projects use any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
8. <span data-ttu-id="29b59-130">Feche o prompt de comando e selecione **criar**  ->  **solução** de compilação *not* (não selecione recompilar solução)</span><span class="sxs-lookup"><span data-stu-id="29b59-130">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution)</span></span>

<span data-ttu-id="29b59-131">Agora você pode pular para [atualizar sua extensão QDK do Visual Studio](#update-visual-studio-qdk-extension).</span><span class="sxs-lookup"><span data-stu-id="29b59-131">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="29b59-132">Atualizar projetos do Q # no Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="29b59-132">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="29b59-133">Em Visual Studio Code, abra a pasta que contém o projeto a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="29b59-133">In Visual Studio Code, open the folder containing the project to update</span></span>
2. <span data-ttu-id="29b59-134">Selecionar **terminal**  ->  **novo terminal**</span><span class="sxs-lookup"><span data-stu-id="29b59-134">Select **Terminal** -> **New Terminal**</span></span>
3. <span data-ttu-id="29b59-135">Siga as instruções para atualizar usando a linha de comando (diretamente abaixo)</span><span class="sxs-lookup"><span data-stu-id="29b59-135">Follow the instructions for updating using the command line (directly below)</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="29b59-136">Atualizar projetos do Q # usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="29b59-136">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="29b59-137">Navegue até a pasta que contém o arquivo de projeto</span><span class="sxs-lookup"><span data-stu-id="29b59-137">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="29b59-138">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="29b59-138">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="29b59-139">Em cada um dos seus arquivos. csproj, atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se for um projeto de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="29b59-139">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="29b59-140">Ou seja, edite as linhas do formulário:</span><span class="sxs-lookup"><span data-stu-id="29b59-140">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="29b59-141">Você pode encontrar mais detalhes sobre como especificar estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="29b59-141">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
4. <span data-ttu-id="29b59-142">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="29b59-142">Run the following command:</span></span>

    ```dotnetcli
    dotnet add package Microsoft.Quantum.Development.Kit
    ```

    <span data-ttu-id="29b59-143">Se seu projeto usar qualquer outro pacote do Microsoft. Quantum (por exemplo, Microsoft. Quantum. Numerics), execute o comando para eles também.</span><span class="sxs-lookup"><span data-stu-id="29b59-143">If your project uses any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
5. <span data-ttu-id="29b59-144">Salve e feche todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="29b59-144">Save and close all files.</span></span>
6. <span data-ttu-id="29b59-145">Repita a 1-4 para cada dependência do projeto e, em seguida, navegue de volta para a pasta que contém o projeto principal e execute:</span><span class="sxs-lookup"><span data-stu-id="29b59-145">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="29b59-146">Com seus projetos do Q # agora atualizados, siga as instruções abaixo para atualizar o próprio QDK.</span><span class="sxs-lookup"><span data-stu-id="29b59-146">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="29b59-147">Atualizando o QDK</span><span class="sxs-lookup"><span data-stu-id="29b59-147">Updating the QDK</span></span>

<span data-ttu-id="29b59-148">O processo para atualizar o QDK varia de acordo com o ambiente e a linguagem de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="29b59-148">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="29b59-149">Selecione seu ambiente de desenvolvimento abaixo.</span><span class="sxs-lookup"><span data-stu-id="29b59-149">Select your development environment below.</span></span>

* [<span data-ttu-id="29b59-150">Python: atualizar a extensão IQ #</span><span class="sxs-lookup"><span data-stu-id="29b59-150">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="29b59-151">Blocos de anotações do Jupyter: Atualize a extensão IQ #</span><span class="sxs-lookup"><span data-stu-id="29b59-151">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="29b59-152">Visual Studio: atualizar a extensão QDK</span><span class="sxs-lookup"><span data-stu-id="29b59-152">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="29b59-153">VS Code: atualizar a extensão QDK</span><span class="sxs-lookup"><span data-stu-id="29b59-153">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="29b59-154">Linha de comando e C#: atualizar modelos de projeto</span><span class="sxs-lookup"><span data-stu-id="29b59-154">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="29b59-155">Atualizar IQ # para Python</span><span class="sxs-lookup"><span data-stu-id="29b59-155">Update IQ# for Python</span></span>

1. <span data-ttu-id="29b59-156">Atualizar o `iqsharp` kernel</span><span class="sxs-lookup"><span data-stu-id="29b59-156">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="29b59-157">Verificar a `iqsharp` versão</span><span class="sxs-lookup"><span data-stu-id="29b59-157">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="29b59-158">Você deve ver o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="29b59-158">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="29b59-159">Não se preocupe se sua `iqsharp` versão for maior, ela deverá corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="29b59-159">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="29b59-160">Atualizar o `qsharp` pacote</span><span class="sxs-lookup"><span data-stu-id="29b59-160">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="29b59-161">Verificar a `qsharp` versão</span><span class="sxs-lookup"><span data-stu-id="29b59-161">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="29b59-162">Você deve ver o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="29b59-162">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="29b59-163">Execute o seguinte comando no local de seus `.qs` arquivos</span><span class="sxs-lookup"><span data-stu-id="29b59-163">Run the following command from the location of your `.qs` files</span></span>

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="29b59-164">Agora você pode usar a versão atualizada do QDK para executar seus programas de Quantum existentes.</span><span class="sxs-lookup"><span data-stu-id="29b59-164">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="29b59-165">Atualizar IQ # para notebooks Jupyter</span><span class="sxs-lookup"><span data-stu-id="29b59-165">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="29b59-166">Atualizar o `iqsharp` kernel</span><span class="sxs-lookup"><span data-stu-id="29b59-166">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="29b59-167">Verificar a `iqsharp` versão</span><span class="sxs-lookup"><span data-stu-id="29b59-167">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="29b59-168">A saída deve ser semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="29b59-168">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="29b59-169">Não se preocupe se sua `iqsharp` versão for maior, ela deverá corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="29b59-169">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="29b59-170">Execute o seguinte comando de uma célula no seu Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="29b59-170">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="29b59-171">Agora você pode abrir um bloco de anotações do Jupyter existente e executá-lo com o QDK atualizado.</span><span class="sxs-lookup"><span data-stu-id="29b59-171">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="29b59-172">Atualizar a extensão QDK do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="29b59-172">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="29b59-173">Atualizar a extensão do Q # Visual Studio</span><span class="sxs-lookup"><span data-stu-id="29b59-173">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="29b59-174">O Visual Studio solicita que você aceite atualizações para a [extensão Quantum do Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="29b59-174">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="29b59-175">Aceitar a atualização</span><span class="sxs-lookup"><span data-stu-id="29b59-175">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="29b59-176">Os modelos de projeto são atualizados com a extensão.</span><span class="sxs-lookup"><span data-stu-id="29b59-176">The project templates are updated with the extension.</span></span> <span data-ttu-id="29b59-177">Os modelos atualizados se aplicam apenas a projetos recém-criados.</span><span class="sxs-lookup"><span data-stu-id="29b59-177">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="29b59-178">O código para seus projetos existentes não é atualizado quando a extensão é atualizada.</span><span class="sxs-lookup"><span data-stu-id="29b59-178">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="29b59-179">Atualizar VS Code extensão QDK</span><span class="sxs-lookup"><span data-stu-id="29b59-179">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="29b59-180">Atualizar a extensão de VS Code Quantum</span><span class="sxs-lookup"><span data-stu-id="29b59-180">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="29b59-181">Reiniciar VS Code</span><span class="sxs-lookup"><span data-stu-id="29b59-181">Restart VS Code</span></span>
    - <span data-ttu-id="29b59-182">Navegue até a guia **extensões**</span><span class="sxs-lookup"><span data-stu-id="29b59-182">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="29b59-183">Selecione o **Microsoft Quantum Development Kit para Visual Studio Code** extensão</span><span class="sxs-lookup"><span data-stu-id="29b59-183">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="29b59-184">Recarregar a extensão</span><span class="sxs-lookup"><span data-stu-id="29b59-184">Reload the extension</span></span>

2. <span data-ttu-id="29b59-185">Atualize os modelos de projeto Quantum:</span><span class="sxs-lookup"><span data-stu-id="29b59-185">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="29b59-186">Ir para **Exibir**  ->  **paleta de comandos**</span><span class="sxs-lookup"><span data-stu-id="29b59-186">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="29b59-187">Selecione **Q #: instalar modelos de projeto**</span><span class="sxs-lookup"><span data-stu-id="29b59-187">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="29b59-188">Após alguns segundos, você deve obter um pop-up confirmando "modelos de projeto instalados com êxito"</span><span class="sxs-lookup"><span data-stu-id="29b59-188">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="29b59-189">C#, usando a `dotnet` ferramenta de linha de comando</span><span class="sxs-lookup"><span data-stu-id="29b59-189">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="29b59-190">Atualizar os modelos de projeto Quantum para .NET</span><span class="sxs-lookup"><span data-stu-id="29b59-190">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```