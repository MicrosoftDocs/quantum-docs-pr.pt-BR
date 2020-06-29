---
title: Atualizar o QDK (Quantum Development Kit)
description: Descreve como atualizar seus projetos Q# e o Microsoft Quantum Development Kit para a versão atual.
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 8d39716c4d4c96ad87862b4b185895aab66cd210
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274014"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="b4154-103">Atualizar o Microsoft QDK (Quantum Development Kit)</span><span class="sxs-lookup"><span data-stu-id="b4154-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="b4154-104">Saiba como atualizar o Microsoft QDK (Quantum Development Kit) para a última versão.</span><span class="sxs-lookup"><span data-stu-id="b4154-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="b4154-105">Este artigo pressupõe que você já tenha o QDK instalado.</span><span class="sxs-lookup"><span data-stu-id="b4154-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="b4154-106">Se você estiver instalando-o pela primeira vez, consulte o [guia de instalação](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="b4154-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="b4154-107">Recomendamos manter-se atualizado com a última versão do QDK.</span><span class="sxs-lookup"><span data-stu-id="b4154-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="b4154-108">Siga este guia de atualização para atualizar o QDK para a última versão.</span><span class="sxs-lookup"><span data-stu-id="b4154-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="b4154-109">O processo consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="b4154-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="b4154-110">Atualização dos arquivos e dos projetos Q# existentes para alinhar o código com qualquer sintaxe atualizada.</span><span class="sxs-lookup"><span data-stu-id="b4154-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="b4154-111">Atualização do próprio QDK para o ambiente de desenvolvimento escolhido.</span><span class="sxs-lookup"><span data-stu-id="b4154-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-q-projects"></a><span data-ttu-id="b4154-112">Atualizar projetos Q#</span><span class="sxs-lookup"><span data-stu-id="b4154-112">Updating Q# Projects</span></span> 

<span data-ttu-id="b4154-113">Independentemente de você estar usando o C# ou o Python para hospedar operações Q#, siga estas instruções para atualizar seus projetos Q#.</span><span class="sxs-lookup"><span data-stu-id="b4154-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="b4154-114">Primeiro, verifique se você tem a última versão do [SDK do .NET Core 3.1](https://dotnet.microsoft.com/download).</span><span class="sxs-lookup"><span data-stu-id="b4154-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="b4154-115">Execute o seguinte comando no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="b4154-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="b4154-116">Verifique se a saída é `3.1.100` ou superior.</span><span class="sxs-lookup"><span data-stu-id="b4154-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="b4154-117">Caso contrário, instale a [última versão](https://dotnet.microsoft.com/download) e verifique novamente.</span><span class="sxs-lookup"><span data-stu-id="b4154-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="b4154-118">Em seguida, siga as instruções abaixo, dependendo da configuração (o Visual Studio, o Visual Studio Code ou diretamente a linha de comando).</span><span class="sxs-lookup"><span data-stu-id="b4154-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="b4154-119">Atualizar projetos Q# no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b4154-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="b4154-120">Atualize para a última versão do Visual Studio 2019. Confira [este link](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="b4154-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="b4154-121">Abra sua solução no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b4154-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="b4154-122">No menu, selecione **Compilar** -> **Limpar Solução**.</span><span class="sxs-lookup"><span data-stu-id="b4154-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="b4154-123">Em cada um dos arquivos .csproj, atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se ela for um projeto de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="b4154-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="b4154-124">Ou seja, edite as linhas do formulário:</span><span class="sxs-lookup"><span data-stu-id="b4154-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="b4154-125">Encontre mais detalhes sobre como especificar as estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="b4154-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="b4154-126">Em cada um dos arquivos .csproj, defina o SDK como `Microsoft.Quantum.Sdk`, conforme indicado na linha abaixo.</span><span class="sxs-lookup"><span data-stu-id="b4154-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="b4154-127">Observe que o número de versão deve ser o último disponível. Determine isso examinando as [notas sobre a versão](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="b4154-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. <span data-ttu-id="b4154-128">Salve e feche todos os arquivos da solução.</span><span class="sxs-lookup"><span data-stu-id="b4154-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="b4154-129">Selecione **Ferramentas** -> **Linha de Comando** -> **Prompt de Comando do Desenvolvedor**.</span><span class="sxs-lookup"><span data-stu-id="b4154-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="b4154-130">Como alternativa, você pode usar o console de gerenciamento de pacotes no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b4154-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="b4154-131">Para cada projeto da solução, execute o seguinte comando para **remover** este pacote:</span><span class="sxs-lookup"><span data-stu-id="b4154-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="b4154-132">Se os projetos usarem outros pacotes Microsoft.Quantum ou Microsoft.Azure.Quantum (por exemplo, Microsoft.Quantum.Numerics), execute o comando **add** neles para atualizar a versão usada.</span><span class="sxs-lookup"><span data-stu-id="b4154-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="b4154-133">Feche o prompt de comando e selecione **Compilar** -> **Compilar Solução** (*não* selecione Recompilar Solução).</span><span class="sxs-lookup"><span data-stu-id="b4154-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="b4154-134">Agora acesse [Atualizar sua extensão do QDK no Visual Studio](#update-visual-studio-qdk-extension).</span><span class="sxs-lookup"><span data-stu-id="b4154-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="b4154-135">Atualizar projetos Q# no Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b4154-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="b4154-136">No Visual Studio Code, abra a pasta que contém o projeto a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="b4154-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="b4154-137">Selecione **Terminal** -> **Novo Terminal**.</span><span class="sxs-lookup"><span data-stu-id="b4154-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="b4154-138">Siga as instruções de atualização usando a linha de comando (diretamente abaixo).</span><span class="sxs-lookup"><span data-stu-id="b4154-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="b4154-139">Atualizar projetos Q# por meio da linha de comando</span><span class="sxs-lookup"><span data-stu-id="b4154-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="b4154-140">Navegue até a pasta que contém o arquivo de projeto principal.</span><span class="sxs-lookup"><span data-stu-id="b4154-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="b4154-141">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="b4154-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="b4154-142">Determine a versão atual do QDK.</span><span class="sxs-lookup"><span data-stu-id="b4154-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="b4154-143">Para encontrá-la, examine as [notas sobre a versão](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="b4154-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="b4154-144">A versão estará em um formato semelhante a `0.11.2006.207`.</span><span class="sxs-lookup"><span data-stu-id="b4154-144">The version will be in a format similar to `0.11.2006.207`.</span></span>

4. <span data-ttu-id="b4154-145">Em cada um dos arquivos `.csproj`, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="b4154-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="b4154-146">Atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se ela for um projeto de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="b4154-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="b4154-147">Ou seja, edite as linhas do formulário:</span><span class="sxs-lookup"><span data-stu-id="b4154-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="b4154-148">Encontre mais detalhes sobre como especificar as estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="b4154-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="b4154-149">Substitua a referência ao SDK na definição de projeto.</span><span class="sxs-lookup"><span data-stu-id="b4154-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="b4154-150">Verifique se o número de versão corresponde ao valor determinado na **etapa 3**.</span><span class="sxs-lookup"><span data-stu-id="b4154-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - <span data-ttu-id="b4154-151">Remova a referência ao pacote `Microsoft.Quantum.Development.Kit`, se presente, que será especificada na seguinte entrada:</span><span class="sxs-lookup"><span data-stu-id="b4154-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="b4154-152">Atualize a versão de todos os pacotes do Microsoft Quantum para a versão lançada mais recentemente do QDK (determinada na **etapa 3**).</span><span class="sxs-lookup"><span data-stu-id="b4154-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="b4154-153">Esses pacotes são nomeados com os seguintes padrões:</span><span class="sxs-lookup"><span data-stu-id="b4154-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="b4154-154">As referências aos pacotes têm o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="b4154-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - <span data-ttu-id="b4154-155">Salve o arquivo atualizado.</span><span class="sxs-lookup"><span data-stu-id="b4154-155">Save the updated file.</span></span>

    - <span data-ttu-id="b4154-156">Restaure as dependências do projeto fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b4154-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="b4154-157">Volte à pasta que contém o projeto principal e execute:</span><span class="sxs-lookup"><span data-stu-id="b4154-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="b4154-158">Com os projetos Q# agora atualizados, siga as instruções abaixo para atualizar o próprio QDK.</span><span class="sxs-lookup"><span data-stu-id="b4154-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="b4154-159">Atualizar o QDK</span><span class="sxs-lookup"><span data-stu-id="b4154-159">Updating the QDK</span></span>

<span data-ttu-id="b4154-160">O processo usado para atualizar o QDK varia de acordo com o ambiente e a linguagem de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="b4154-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="b4154-161">Selecione o ambiente de desenvolvimento abaixo.</span><span class="sxs-lookup"><span data-stu-id="b4154-161">Select your development environment below.</span></span>

* [<span data-ttu-id="b4154-162">Python: atualizar a extensão do IQ#</span><span class="sxs-lookup"><span data-stu-id="b4154-162">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="b4154-163">Jupyter Notebooks: atualizar a extensão do IQ#</span><span class="sxs-lookup"><span data-stu-id="b4154-163">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="b4154-164">Visual Studio: atualizar a extensão do QDK</span><span class="sxs-lookup"><span data-stu-id="b4154-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="b4154-165">VS Code: atualizar a extensão do QDK</span><span class="sxs-lookup"><span data-stu-id="b4154-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="b4154-166">Linha de comando e C#: atualizar modelos de projeto</span><span class="sxs-lookup"><span data-stu-id="b4154-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="b4154-167">Atualizar o IQ# para Python</span><span class="sxs-lookup"><span data-stu-id="b4154-167">Update IQ# for Python</span></span>

1. <span data-ttu-id="b4154-168">Atualize o kernel `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="b4154-168">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="b4154-169">Verifique a versão `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="b4154-169">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="b4154-170">Você deve ver o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="b4154-170">You should see the following output:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="b4154-171">Não se preocupe se a versão do `iqsharp` for superior; ela deverá corresponder à [última versão](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="b4154-171">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="b4154-172">Atualize o pacote `qsharp`</span><span class="sxs-lookup"><span data-stu-id="b4154-172">Update the `qsharp` package</span></span>

    ```
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="b4154-173">Verifique a versão `qsharp`</span><span class="sxs-lookup"><span data-stu-id="b4154-173">Verify the `qsharp` version</span></span>

    ```
    pip show qsharp
    ```

    <span data-ttu-id="b4154-174">Você deve ver o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="b4154-174">You should see the following output:</span></span>

    ```
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="b4154-175">Execute o comando a seguir na localização dos arquivos `.qs`</span><span class="sxs-lookup"><span data-stu-id="b4154-175">Run the following command from the location of your `.qs` files</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="b4154-176">Agora você pode usar a versão atualizada do QDK para executar seus programas quânticos existentes.</span><span class="sxs-lookup"><span data-stu-id="b4154-176">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="b4154-177">Atualizar o IQ# para Jupyter Notebooks</span><span class="sxs-lookup"><span data-stu-id="b4154-177">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="b4154-178">Atualize o kernel `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="b4154-178">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="b4154-179">Verifique a versão `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="b4154-179">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="b4154-180">A saída deve ser semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="b4154-180">Your output should be similar to the following:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="b4154-181">Não se preocupe se a versão do `iqsharp` for superior; ela deverá corresponder à [última versão](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="b4154-181">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="b4154-182">Execute o seguinte comando em uma célula do Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="b4154-182">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="b4154-183">Agora você pode abrir um Jupyter notebook existente e executá-lo com o QDK atualizado.</span><span class="sxs-lookup"><span data-stu-id="b4154-183">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="b4154-184">Atualizar a extensão do QDK para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b4154-184">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="b4154-185">Atualizar a extensão do Q# para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b4154-185">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="b4154-186">O Visual Studio exibe um aviso solicitando que você aceite as atualizações da [extensão do Quantum no Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="b4154-186">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="b4154-187">Aceite a atualização</span><span class="sxs-lookup"><span data-stu-id="b4154-187">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4154-188">Os modelos de projeto serão atualizados com a extensão.</span><span class="sxs-lookup"><span data-stu-id="b4154-188">The project templates are updated with the extension.</span></span> <span data-ttu-id="b4154-189">Os modelos atualizados se aplicam apenas aos projetos recém-criados.</span><span class="sxs-lookup"><span data-stu-id="b4154-189">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="b4154-190">O código para os projetos existentes não é atualizado quando a extensão é atualizada.</span><span class="sxs-lookup"><span data-stu-id="b4154-190">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="b4154-191">Atualizar a extensão do QDK para VS Code</span><span class="sxs-lookup"><span data-stu-id="b4154-191">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="b4154-192">Atualize a extensão do Quantum para VS Code</span><span class="sxs-lookup"><span data-stu-id="b4154-192">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="b4154-193">Reinicie o VS Code</span><span class="sxs-lookup"><span data-stu-id="b4154-193">Restart VS Code</span></span>
    - <span data-ttu-id="b4154-194">Navegue até a guia **Extensões**</span><span class="sxs-lookup"><span data-stu-id="b4154-194">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="b4154-195">Selecione a extensão **Microsoft Quantum Development Kit para Visual Studio Code**</span><span class="sxs-lookup"><span data-stu-id="b4154-195">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="b4154-196">Recarregue a extensão</span><span class="sxs-lookup"><span data-stu-id="b4154-196">Reload the extension</span></span>

2. <span data-ttu-id="b4154-197">Atualize os modelos de projeto do Quantum:</span><span class="sxs-lookup"><span data-stu-id="b4154-197">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="b4154-198">Acesse **Exibir** -> **Paleta de Comandos**</span><span class="sxs-lookup"><span data-stu-id="b4154-198">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="b4154-199">Selecione **Q#: Instalar modelos de projeto**</span><span class="sxs-lookup"><span data-stu-id="b4154-199">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="b4154-200">Após alguns segundos, você verá um pop-up com a mensagem "Modelos de projeto instalados com êxito"</span><span class="sxs-lookup"><span data-stu-id="b4154-200">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="b4154-201">C#, usando a ferramenta de linha de comando `dotnet`</span><span class="sxs-lookup"><span data-stu-id="b4154-201">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="b4154-202">Atualizar os modelos de projeto do Quantum para .NET</span><span class="sxs-lookup"><span data-stu-id="b4154-202">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
