---
title: Atualizar o kit de desenvolvimento Quantum (QDK)
description: 'Descreve como atualizar seus projetos do Q # e o Microsoft Quantum Development Kit para a versão atual.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 3245f587493ce12cfec15c8f932fd092d85f688e
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327554"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="1e1fd-103">Atualizar o Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="1e1fd-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="1e1fd-104">Saiba como atualizar o Microsoft Quantum Development Kit (QDK) para a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="1e1fd-105">Este artigo pressupõe que você já tenha o QDK instalado.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="1e1fd-106">Se você estiver instalando o pela primeira vez, consulte o guia de [instalação](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="1e1fd-107">É recomendável manter-se atualizado com a versão mais recente do QDK.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="1e1fd-108">Siga este guia de atualização para atualizar para a versão mais recente do QDK.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="1e1fd-109">O processo consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="1e1fd-110">Atualizando seus arquivos e projetos do Q # existentes para alinhar seu código com qualquer sintaxe atualizada.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="1e1fd-111">Atualizar o próprio QDK para o ambiente de desenvolvimento escolhido.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-q-projects"></a><span data-ttu-id="1e1fd-112">Atualizando projetos de Q #</span><span class="sxs-lookup"><span data-stu-id="1e1fd-112">Updating Q# Projects</span></span> 

<span data-ttu-id="1e1fd-113">Independentemente de você estar usando C# ou Python para hospedar operações Q #, siga estas instruções para atualizar seus projetos do Q #.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="1e1fd-114">Primeiro, verifique se você tem a versão mais recente do [SDK do .NET Core 3,1](https://dotnet.microsoft.com/download).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="1e1fd-115">Execute o seguinte comando no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="1e1fd-116">Verifique se a saída é `3.1.100` ou mais alta.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="1e1fd-117">Caso contrário, instale a [versão mais recente](https://dotnet.microsoft.com/download) e verifique novamente.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="1e1fd-118">Em seguida, siga as instruções abaixo, dependendo da sua configuração (Visual Studio, Visual Studio Code ou diretamente a linha de comando).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="1e1fd-119">Atualizar projetos do Q # no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1e1fd-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="1e1fd-120">Atualize para a versão mais recente do Visual Studio 2019, consulte [aqui](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="1e1fd-121">Abra sua solução no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="1e1fd-122">No menu, selecione **criar**  ->  **solução limpa**.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="1e1fd-123">Em cada um dos seus arquivos. csproj, atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se for um projeto de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="1e1fd-124">Ou seja, edite as linhas do formulário:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="1e1fd-125">Você pode encontrar mais detalhes sobre como especificar estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="1e1fd-126">Em cada um dos arquivos. csproj, defina o SDK `Microsoft.Quantum.Sdk` como, conforme indicado na linha abaixo.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="1e1fd-127">Observe que o número de versão deve ser o mais recente disponível e você pode determinar isso revisando as [notas de versão](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. <span data-ttu-id="1e1fd-128">Salve e feche todos os arquivos em sua solução.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="1e1fd-129">Selecione **ferramentas**  ->  prompt de comando do desenvolvedor de**linha de comando**  ->  **Developer Command Prompt**.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="1e1fd-130">Como alternativa, você pode usar o console de gerenciamento de pacotes no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="1e1fd-131">Para cada projeto na solução, execute o seguinte comando para **remover** este pacote:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="1e1fd-132">Se seus projetos usarem outros pacotes Microsoft. Quantum ou Microsoft. Azure. Quantum (por exemplo, Microsoft. Quantum. Numerics), execute o comando **Add** para que eles atualizem a versão usada.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="1e1fd-133">Feche o prompt de comando e selecione **criar**  ->  **solução** de compilação *not* (não selecione recompilar solução).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="1e1fd-134">Agora você pode pular para [atualizar sua extensão QDK do Visual Studio](#update-visual-studio-qdk-extension).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="1e1fd-135">Atualizar projetos do Q # no Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="1e1fd-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="1e1fd-136">Em Visual Studio Code, abra a pasta que contém o projeto a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="1e1fd-137">Selecione **terminal**  ->  **novo terminal**.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="1e1fd-138">Siga as instruções para atualizar usando a linha de comando (diretamente abaixo).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="1e1fd-139">Atualizar projetos do Q # usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="1e1fd-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="1e1fd-140">Navegue até a pasta que contém o arquivo de projeto principal.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="1e1fd-141">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="1e1fd-142">Determine a versão atual do QDK.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="1e1fd-143">Para encontrá-lo, você pode revisar as [notas de versão](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="1e1fd-144">A versão estará em um formato semelhante a `0.11.2006.207` .</span><span class="sxs-lookup"><span data-stu-id="1e1fd-144">The version will be in a format similar to `0.11.2006.207`.</span></span>

4. <span data-ttu-id="1e1fd-145">Em cada um de seus `.csproj` arquivos, percorra as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="1e1fd-146">Atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se for um projeto de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="1e1fd-147">Ou seja, edite as linhas do formulário:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="1e1fd-148">Você pode encontrar mais detalhes sobre como especificar estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="1e1fd-149">Substitua a referência ao SDK na definição do projeto.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="1e1fd-150">Certifique-se de que o número de versão corresponde ao valor determinado na **etapa 3**.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - <span data-ttu-id="1e1fd-151">Remova a referência ao pacote `Microsoft.Quantum.Development.Kit` , se presente, que será especificado na seguinte entrada:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="1e1fd-152">Atualize a versão de todos os pacotes Quantum da Microsoft para a versão lançada mais recentemente do QDK (determinado na **etapa 3**).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="1e1fd-153">Esses pacotes são nomeados com os seguintes padrões:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="1e1fd-154">As referências a pacotes têm o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - <span data-ttu-id="1e1fd-155">Salve o arquivo atualizado.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-155">Save the updated file.</span></span>

    - <span data-ttu-id="1e1fd-156">Restaure as dependências do projeto, fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="1e1fd-157">Navegue de volta para a pasta que contém o projeto principal e execute:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="1e1fd-158">Com seus projetos do Q # agora atualizados, siga as instruções abaixo para atualizar o próprio QDK.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="1e1fd-159">Atualizando o QDK</span><span class="sxs-lookup"><span data-stu-id="1e1fd-159">Updating the QDK</span></span>

<span data-ttu-id="1e1fd-160">O processo para atualizar o QDK varia de acordo com o ambiente e a linguagem de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="1e1fd-161">Selecione seu ambiente de desenvolvimento abaixo.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-161">Select your development environment below.</span></span>

* [<span data-ttu-id="1e1fd-162">Python: atualizar a extensão IQ #</span><span class="sxs-lookup"><span data-stu-id="1e1fd-162">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="1e1fd-163">Blocos de anotações do Jupyter: Atualize a extensão IQ #</span><span class="sxs-lookup"><span data-stu-id="1e1fd-163">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="1e1fd-164">Visual Studio: atualizar a extensão QDK</span><span class="sxs-lookup"><span data-stu-id="1e1fd-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="1e1fd-165">VS Code: atualizar a extensão QDK</span><span class="sxs-lookup"><span data-stu-id="1e1fd-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="1e1fd-166">Linha de comando e C#: atualizar modelos de projeto</span><span class="sxs-lookup"><span data-stu-id="1e1fd-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="1e1fd-167">Atualizar IQ # para Python</span><span class="sxs-lookup"><span data-stu-id="1e1fd-167">Update IQ# for Python</span></span>

1. <span data-ttu-id="1e1fd-168">Atualizar o `iqsharp` kernel</span><span class="sxs-lookup"><span data-stu-id="1e1fd-168">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="1e1fd-169">Verificar a `iqsharp` versão</span><span class="sxs-lookup"><span data-stu-id="1e1fd-169">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="1e1fd-170">Você deve ver o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-170">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="1e1fd-171">Não se preocupe se sua `iqsharp` versão for maior, ela deverá corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-171">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="1e1fd-172">Atualizar o `qsharp` pacote</span><span class="sxs-lookup"><span data-stu-id="1e1fd-172">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="1e1fd-173">Verificar a `qsharp` versão</span><span class="sxs-lookup"><span data-stu-id="1e1fd-173">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="1e1fd-174">Você deve ver o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-174">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="1e1fd-175">Execute o seguinte comando no local de seus `.qs` arquivos</span><span class="sxs-lookup"><span data-stu-id="1e1fd-175">Run the following command from the location of your `.qs` files</span></span>

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="1e1fd-176">Agora você pode usar a versão atualizada do QDK para executar seus programas de Quantum existentes.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-176">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="1e1fd-177">Atualizar IQ # para notebooks Jupyter</span><span class="sxs-lookup"><span data-stu-id="1e1fd-177">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="1e1fd-178">Atualizar o `iqsharp` kernel</span><span class="sxs-lookup"><span data-stu-id="1e1fd-178">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="1e1fd-179">Verificar a `iqsharp` versão</span><span class="sxs-lookup"><span data-stu-id="1e1fd-179">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="1e1fd-180">A saída deve ser semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-180">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="1e1fd-181">Não se preocupe se sua `iqsharp` versão for maior, ela deverá corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="1e1fd-181">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="1e1fd-182">Execute o seguinte comando de uma célula no seu Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-182">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="1e1fd-183">Agora você pode abrir um bloco de anotações do Jupyter existente e executá-lo com o QDK atualizado.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-183">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="1e1fd-184">Atualizar a extensão QDK do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1e1fd-184">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="1e1fd-185">Atualizar a extensão do Q # Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1e1fd-185">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="1e1fd-186">O Visual Studio solicita que você aceite atualizações para a [extensão Quantum do Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="1e1fd-186">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="1e1fd-187">Aceitar a atualização</span><span class="sxs-lookup"><span data-stu-id="1e1fd-187">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e1fd-188">Os modelos de projeto são atualizados com a extensão.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-188">The project templates are updated with the extension.</span></span> <span data-ttu-id="1e1fd-189">Os modelos atualizados se aplicam apenas a projetos recém-criados.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-189">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="1e1fd-190">O código para seus projetos existentes não é atualizado quando a extensão é atualizada.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-190">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="1e1fd-191">Atualizar VS Code extensão QDK</span><span class="sxs-lookup"><span data-stu-id="1e1fd-191">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="1e1fd-192">Atualizar a extensão de VS Code Quantum</span><span class="sxs-lookup"><span data-stu-id="1e1fd-192">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="1e1fd-193">Reiniciar VS Code</span><span class="sxs-lookup"><span data-stu-id="1e1fd-193">Restart VS Code</span></span>
    - <span data-ttu-id="1e1fd-194">Navegue até a guia **extensões**</span><span class="sxs-lookup"><span data-stu-id="1e1fd-194">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="1e1fd-195">Selecione o **Microsoft Quantum Development Kit para Visual Studio Code** extensão</span><span class="sxs-lookup"><span data-stu-id="1e1fd-195">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="1e1fd-196">Recarregar a extensão</span><span class="sxs-lookup"><span data-stu-id="1e1fd-196">Reload the extension</span></span>

2. <span data-ttu-id="1e1fd-197">Atualize os modelos de projeto Quantum:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-197">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="1e1fd-198">Ir para **Exibir**  ->  **paleta de comandos**</span><span class="sxs-lookup"><span data-stu-id="1e1fd-198">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="1e1fd-199">Selecione **Q #: instalar modelos de projeto**</span><span class="sxs-lookup"><span data-stu-id="1e1fd-199">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="1e1fd-200">Após alguns segundos, você deve obter um pop-up confirmando "modelos de projeto instalados com êxito"</span><span class="sxs-lookup"><span data-stu-id="1e1fd-200">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="1e1fd-201">C#, usando a `dotnet` ferramenta de linha de comando</span><span class="sxs-lookup"><span data-stu-id="1e1fd-201">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="1e1fd-202">Atualizar os modelos de projeto Quantum para .NET</span><span class="sxs-lookup"><span data-stu-id="1e1fd-202">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
