---
title: Atualizar o QDK (Quantum Development Kit)
description: Descreve como atualizar projetos do Q# e o Microsoft Quantum Development Kit para a versão atual.
author: bradben
ms.author: v-benbra
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
no-loc:
- Q#
- $$v
ms.openlocfilehash: d9678a61f5fe4ca466b6a84e9e4b68321c5baee3
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834906"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="4235a-103">Atualizar o Microsoft QDK (Quantum Development Kit)</span><span class="sxs-lookup"><span data-stu-id="4235a-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="4235a-104">Saiba como atualizar o Microsoft QDK (Quantum Development Kit) para a última versão.</span><span class="sxs-lookup"><span data-stu-id="4235a-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="4235a-105">Este artigo pressupõe que você já tenha o QDK instalado.</span><span class="sxs-lookup"><span data-stu-id="4235a-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="4235a-106">Se você estiver instalando-o pela primeira vez, consulte o [guia de instalação](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="4235a-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="4235a-107">Recomendamos manter-se atualizado com a última versão do QDK.</span><span class="sxs-lookup"><span data-stu-id="4235a-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="4235a-108">Siga este guia de atualização para atualizar o QDK para a última versão.</span><span class="sxs-lookup"><span data-stu-id="4235a-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="4235a-109">O processo consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="4235a-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="4235a-110">Atualizar os arquivos e os projetos Q# existentes para alinhar o código com qualquer sintaxe atualizada.</span><span class="sxs-lookup"><span data-stu-id="4235a-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="4235a-111">Atualização do próprio QDK para o ambiente de desenvolvimento escolhido.</span><span class="sxs-lookup"><span data-stu-id="4235a-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-no-locq-projects"></a><span data-ttu-id="4235a-112">Atualizar projetos do Q#</span><span class="sxs-lookup"><span data-stu-id="4235a-112">Updating Q# Projects</span></span> 

<span data-ttu-id="4235a-113">Independentemente de você estar usando o C# ou o Python para hospedar operações Q#, siga estas instruções para atualizar projetos do Q#.</span><span class="sxs-lookup"><span data-stu-id="4235a-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="4235a-114">Primeiro, verifique se você tem a última versão do [SDK do .NET Core 3.1](https://dotnet.microsoft.com/download).</span><span class="sxs-lookup"><span data-stu-id="4235a-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="4235a-115">Execute o seguinte comando no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="4235a-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="4235a-116">Verifique se a saída é `3.1.100` ou superior.</span><span class="sxs-lookup"><span data-stu-id="4235a-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="4235a-117">Caso contrário, instale a [última versão](https://dotnet.microsoft.com/download) e verifique novamente.</span><span class="sxs-lookup"><span data-stu-id="4235a-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="4235a-118">Em seguida, siga as instruções abaixo, dependendo da configuração (o Visual Studio, o Visual Studio Code ou diretamente no prompt de comando).</span><span class="sxs-lookup"><span data-stu-id="4235a-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly from the command prompt).</span></span>

### <a name="update-no-locq-projects-in-visual-studio"></a><span data-ttu-id="4235a-119">Atualizar projetos do Q# no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4235a-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="4235a-120">Atualize para a última versão do Visual Studio 2019. Confira [este link](https://docs.microsoft.com/visualstudio/install/update-visual-studio) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="4235a-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio) for instructions.</span></span>
2. <span data-ttu-id="4235a-121">Abra sua solução no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4235a-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="4235a-122">No menu, selecione **Compilar** -> **Limpar Solução**.</span><span class="sxs-lookup"><span data-stu-id="4235a-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="4235a-123">Em cada um dos arquivos .csproj, atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se ela for um projeto de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="4235a-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="4235a-124">Ou seja, edite as linhas do formulário:</span><span class="sxs-lookup"><span data-stu-id="4235a-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="4235a-125">Encontre mais detalhes sobre como especificar as estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="4235a-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="4235a-126">Em cada um dos arquivos .csproj, defina o SDK como `Microsoft.Quantum.Sdk`, conforme indicado na linha abaixo.</span><span class="sxs-lookup"><span data-stu-id="4235a-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="4235a-127">Observe que o número de versão deve ser o último disponível. Determine isso examinando as [notas sobre a versão](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="4235a-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    ```

6. <span data-ttu-id="4235a-128">Salve e feche todos os arquivos da solução.</span><span class="sxs-lookup"><span data-stu-id="4235a-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="4235a-129">Selecione **Ferramentas** -> **Linha de Comando** -> **Prompt de Comando do Desenvolvedor**.</span><span class="sxs-lookup"><span data-stu-id="4235a-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="4235a-130">Como alternativa, você pode usar o console de gerenciamento de pacotes no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4235a-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="4235a-131">Para cada projeto da solução, execute o seguinte comando para **remover** este pacote:</span><span class="sxs-lookup"><span data-stu-id="4235a-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="4235a-132">Se os projetos usarem outros pacotes Microsoft.Quantum ou Microsoft.Azure.Quantum (por exemplo, Microsoft.Quantum.Numerics), execute o comando **add** neles para atualizar a versão usada.</span><span class="sxs-lookup"><span data-stu-id="4235a-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="4235a-133">Feche o prompt de comando e selecione **Compilar** -> **Compilar Solução** (*não* selecione Recompilar Solução).</span><span class="sxs-lookup"><span data-stu-id="4235a-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="4235a-134">Agora acesse [Atualizar sua extensão do QDK no Visual Studio](#update-visual-studio-qdk-extension).</span><span class="sxs-lookup"><span data-stu-id="4235a-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-no-locq-projects-in-visual-studio-code"></a><span data-ttu-id="4235a-135">Atualizar projetos do Q# no Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="4235a-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="4235a-136">No Visual Studio Code, abra a pasta que contém o projeto a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4235a-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="4235a-137">Selecione **Terminal** -> **Novo Terminal**.</span><span class="sxs-lookup"><span data-stu-id="4235a-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="4235a-138">Siga as instruções de atualização usando o prompt de comando (diretamente abaixo).</span><span class="sxs-lookup"><span data-stu-id="4235a-138">Follow the instructions for updating using the command prompt (directly below).</span></span>

### <a name="update-no-locq-projects-using-the-command-prompt"></a><span data-ttu-id="4235a-139">Atualizar projetos Q# no prompt de comando</span><span class="sxs-lookup"><span data-stu-id="4235a-139">Update Q# projects using the command prompt</span></span>

1. <span data-ttu-id="4235a-140">Navegue até a pasta que contém o arquivo de projeto principal.</span><span class="sxs-lookup"><span data-stu-id="4235a-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="4235a-141">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="4235a-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="4235a-142">Determine a versão atual do QDK.</span><span class="sxs-lookup"><span data-stu-id="4235a-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="4235a-143">Para encontrá-la, examine as [notas sobre a versão](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="4235a-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="4235a-144">A versão estará em um formato semelhante a `0.12.20072031`.</span><span class="sxs-lookup"><span data-stu-id="4235a-144">The version will be in a format similar to `0.12.20072031`.</span></span>

4. <span data-ttu-id="4235a-145">Em cada um dos arquivos `.csproj`, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="4235a-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="4235a-146">Atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se ela for um projeto de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="4235a-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="4235a-147">Ou seja, edite as linhas do formulário:</span><span class="sxs-lookup"><span data-stu-id="4235a-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="4235a-148">Encontre mais detalhes sobre como especificar as estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="4235a-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="4235a-149">Substitua a referência ao SDK na definição de projeto.</span><span class="sxs-lookup"><span data-stu-id="4235a-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="4235a-150">Verifique se o número de versão corresponde ao valor determinado na **etapa 3**.</span><span class="sxs-lookup"><span data-stu-id="4235a-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
        ```

    - <span data-ttu-id="4235a-151">Remova a referência ao pacote `Microsoft.Quantum.Development.Kit`, se presente, que será especificada na seguinte entrada:</span><span class="sxs-lookup"><span data-stu-id="4235a-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="4235a-152">Atualize a versão de todos os pacotes do Microsoft Quantum para a versão lançada mais recentemente do QDK (determinada na **etapa 3**).</span><span class="sxs-lookup"><span data-stu-id="4235a-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="4235a-153">Esses pacotes são nomeados com os seguintes padrões:</span><span class="sxs-lookup"><span data-stu-id="4235a-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="4235a-154">As referências aos pacotes têm o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="4235a-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.12.20072031" />
        ```

    - <span data-ttu-id="4235a-155">Salve o arquivo atualizado.</span><span class="sxs-lookup"><span data-stu-id="4235a-155">Save the updated file.</span></span>

    - <span data-ttu-id="4235a-156">Restaure as dependências do projeto fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4235a-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="4235a-157">Volte à pasta que contém o projeto principal e execute:</span><span class="sxs-lookup"><span data-stu-id="4235a-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="4235a-158">Com os projetos do Q# atualizados, siga estas instruções para atualizar o próprio QDK.</span><span class="sxs-lookup"><span data-stu-id="4235a-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="4235a-159">Atualizar o QDK</span><span class="sxs-lookup"><span data-stu-id="4235a-159">Updating the QDK</span></span>

<span data-ttu-id="4235a-160">O processo usado para atualizar o QDK varia de acordo com o ambiente e a linguagem de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="4235a-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="4235a-161">Selecione o ambiente de desenvolvimento abaixo.</span><span class="sxs-lookup"><span data-stu-id="4235a-161">Select your development environment below.</span></span>

* [<span data-ttu-id="4235a-162">Python: atualizar o pacote `qsharp`</span><span class="sxs-lookup"><span data-stu-id="4235a-162">Python: update the `qsharp` package</span></span>](#update-the-qsharp-python-package)
* [<span data-ttu-id="4235a-163">Jupyter Notebooks: atualizar o kernel do IQ#</span><span class="sxs-lookup"><span data-stu-id="4235a-163">Jupyter Notebooks: update the IQ# kernel</span></span>](#update-the-iq-jupyter-kernel)
* [<span data-ttu-id="4235a-164">Visual Studio: atualizar a extensão do QDK</span><span class="sxs-lookup"><span data-stu-id="4235a-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="4235a-165">VS Code: atualizar a extensão do QDK</span><span class="sxs-lookup"><span data-stu-id="4235a-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="4235a-166">Linha de comando e C#: atualizar modelos de projeto</span><span class="sxs-lookup"><span data-stu-id="4235a-166">Command line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-the-qsharp-python-package"></a><span data-ttu-id="4235a-167">Atualizar o pacote `qsharp` do Python</span><span class="sxs-lookup"><span data-stu-id="4235a-167">Update the `qsharp` Python package</span></span>

<span data-ttu-id="4235a-168">O procedimento de atualização depende de a instalação original ter sido feita usando o conda ou a CLI do .NET e o pip.</span><span class="sxs-lookup"><span data-stu-id="4235a-168">The update procedure depends on whether you originally installed using conda or using the .NET CLI and pip.</span></span>

#### <a name="update-using-conda-recommended"></a>[<span data-ttu-id="4235a-169">Atualizar usando o conda (recomendado)</span><span class="sxs-lookup"><span data-stu-id="4235a-169">Update using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="4235a-170">Ative o ambiente de conda em que você instalou o pacote `qsharp` e execute este comando para atualizá-lo:</span><span class="sxs-lookup"><span data-stu-id="4235a-170">Activate the conda environment where you installed the `qsharp` package, and then run this command to update it:</span></span>

    ```
    conda update -c quantum-engineering qsharp
    ```

1. <span data-ttu-id="4235a-171">Execute o comando a seguir no local dos arquivos `.qs`:</span><span class="sxs-lookup"><span data-stu-id="4235a-171">Run the following command from the location of your `.qs` files:</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="4235a-172">Atualizar usando a CLI do .NET e o pip (avançado)</span><span class="sxs-lookup"><span data-stu-id="4235a-172">Update using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="4235a-173">Atualize o kernel `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="4235a-173">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="4235a-174">Verifique a versão `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="4235a-174">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="4235a-175">Você deve ver o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="4235a-175">You should see the following output:</span></span>

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    <span data-ttu-id="4235a-176">Não se preocupe se sua versão do `iqsharp` for maior.</span><span class="sxs-lookup"><span data-stu-id="4235a-176">Don't worry if your `iqsharp` version is higher.</span></span> <span data-ttu-id="4235a-177">Ela deve corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="4235a-177">It should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

1. <span data-ttu-id="4235a-178">Atualize o pacote `qsharp`:</span><span class="sxs-lookup"><span data-stu-id="4235a-178">Update the `qsharp` package:</span></span>

    ```
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="4235a-179">Verifique a versão `qsharp`:</span><span class="sxs-lookup"><span data-stu-id="4235a-179">Verify the `qsharp` version:</span></span>

    ```
    pip show qsharp
    ```

    <span data-ttu-id="4235a-180">Você deve ver o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="4235a-180">You should see the following output:</span></span>

    ```
    Name: qsharp
    Version: 0.12.2007.2031
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. <span data-ttu-id="4235a-181">Execute o comando a seguir no local dos arquivos `.qs`:</span><span class="sxs-lookup"><span data-stu-id="4235a-181">Run the following command from the location of your `.qs` files:</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

***

<span data-ttu-id="4235a-182">Agora você pode usar o pacote `qsharp` do Python atualizado para executar seus programas quânticos existentes.</span><span class="sxs-lookup"><span data-stu-id="4235a-182">You can now use the updated `qsharp` Python package to run your existing quantum programs.</span></span>

### <a name="update-the-ino-locq-jupyter-kernel"></a><span data-ttu-id="4235a-183">Atualizar o kernel de Jupyter do IQ#</span><span class="sxs-lookup"><span data-stu-id="4235a-183">Update the IQ# Jupyter kernel</span></span>

<span data-ttu-id="4235a-184">O procedimento de atualização depende de a instalação original ter sido feita usando o conda ou a CLI do .NET e o pip.</span><span class="sxs-lookup"><span data-stu-id="4235a-184">The update procedure depends on whether you originally installed using conda or using the .NET CLI and pip.</span></span>

#### <a name="update-using-conda-recommended"></a>[<span data-ttu-id="4235a-185">Atualizar usando o conda (recomendado)</span><span class="sxs-lookup"><span data-stu-id="4235a-185">Update using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="4235a-186">Ative o ambiente de conda em que você instalou o pacote `qsharp` e execute este comando para atualizá-lo:</span><span class="sxs-lookup"><span data-stu-id="4235a-186">Activate the conda environment where you installed the `qsharp` package, and then run this command to update it:</span></span>

    ```
    conda update -c quantum-engineering qsharp
    ```

1. <span data-ttu-id="4235a-187">Execute o seguinte comando em uma célula em cada um dos Jupyter Notebooks do Q# existentes:</span><span class="sxs-lookup"><span data-stu-id="4235a-187">Run the following command from a cell in each of your existing Q# Jupyter Notebooks:</span></span>

    ```
    %workspace reload
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="4235a-188">Atualizar usando a CLI do .NET e o pip (avançado)</span><span class="sxs-lookup"><span data-stu-id="4235a-188">Update using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="4235a-189">Atualize o pacote `Microsoft.Quantum.IQSharp`:</span><span class="sxs-lookup"><span data-stu-id="4235a-189">Update the `Microsoft.Quantum.IQSharp` package:</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="4235a-190">Verifique a versão `iqsharp`:</span><span class="sxs-lookup"><span data-stu-id="4235a-190">Verify the `iqsharp` version:</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="4235a-191">A saída deve ser semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="4235a-191">Your output should be similar to the following:</span></span>

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    <span data-ttu-id="4235a-192">Não se preocupe se sua versão do `iqsharp` for maior.</span><span class="sxs-lookup"><span data-stu-id="4235a-192">Don't worry if your `iqsharp` version is higher.</span></span> <span data-ttu-id="4235a-193">Ela deve corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="4235a-193">It should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

1. <span data-ttu-id="4235a-194">Execute o seguinte comando em uma célula em cada um dos Jupyter Notebooks do Q# existentes:</span><span class="sxs-lookup"><span data-stu-id="4235a-194">Run the following command from a cell in each of your existing Q# Jupyter Notebooks:</span></span>

    ```
    %workspace reload
    ```

***

<span data-ttu-id="4235a-195">Agora você pode usar o kernel do IQ# atualizado para executar os Jupyter Notebooks existentes do Q#.</span><span class="sxs-lookup"><span data-stu-id="4235a-195">You can now use the updated IQ# kernel to run your existing Q# Jupyter Notebooks.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="4235a-196">Atualizar a extensão do QDK para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4235a-196">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="4235a-197">Atualizar a extensão do Visual Studio do Q#</span><span class="sxs-lookup"><span data-stu-id="4235a-197">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="4235a-198">O Visual Studio exibe um aviso solicitando que você aceite as atualizações da [extensão do Quantum no Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="4235a-198">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="4235a-199">Aceite a atualização</span><span class="sxs-lookup"><span data-stu-id="4235a-199">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="4235a-200">Os modelos de projeto serão atualizados com a extensão.</span><span class="sxs-lookup"><span data-stu-id="4235a-200">The project templates are updated with the extension.</span></span> <span data-ttu-id="4235a-201">Os modelos atualizados se aplicam apenas aos projetos recém-criados.</span><span class="sxs-lookup"><span data-stu-id="4235a-201">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="4235a-202">O código para os projetos existentes não é atualizado quando a extensão é atualizada.</span><span class="sxs-lookup"><span data-stu-id="4235a-202">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="4235a-203">Atualizar a extensão do QDK para VS Code</span><span class="sxs-lookup"><span data-stu-id="4235a-203">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="4235a-204">Atualize a extensão do Quantum para VS Code</span><span class="sxs-lookup"><span data-stu-id="4235a-204">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="4235a-205">Reinicie o VS Code</span><span class="sxs-lookup"><span data-stu-id="4235a-205">Restart VS Code</span></span>
    - <span data-ttu-id="4235a-206">Navegue até a guia **Extensões**</span><span class="sxs-lookup"><span data-stu-id="4235a-206">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="4235a-207">Selecione a extensão **Microsoft Quantum Development Kit para Visual Studio Code**</span><span class="sxs-lookup"><span data-stu-id="4235a-207">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="4235a-208">Recarregue a extensão</span><span class="sxs-lookup"><span data-stu-id="4235a-208">Reload the extension</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="4235a-209">C#, usando a ferramenta de linha de comando `dotnet`</span><span class="sxs-lookup"><span data-stu-id="4235a-209">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="4235a-210">Atualizar os modelos de projeto do Quantum para .NET</span><span class="sxs-lookup"><span data-stu-id="4235a-210">Update the Quantum project templates for .NET</span></span>

    <span data-ttu-id="4235a-211">No prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="4235a-211">From the command prompt:</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

   <span data-ttu-id="4235a-212">Como alternativa, se você pretende usar os modelos de linha de comando e já tiver a extensão VS Code QDK instalada, atualize os modelos de projeto da própria extensão:</span><span class="sxs-lookup"><span data-stu-id="4235a-212">Alternatively, if you intend to use the command-line templates, and already have the VS Code QDK extension installed, you can update the project templates from the extension itself:</span></span>

   - [<span data-ttu-id="4235a-213">Atualizar a extensão QDK</span><span class="sxs-lookup"><span data-stu-id="4235a-213">Update the QDK extension</span></span>](#update-vs-code-qdk-extension)
   - <span data-ttu-id="4235a-214">No VS Code, acesse **Exibir** -> **Paleta de Comandos**</span><span class="sxs-lookup"><span data-stu-id="4235a-214">In VS Code, go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="4235a-215">Selecione **Q#: Instalar modelos de projeto de linha de comando**</span><span class="sxs-lookup"><span data-stu-id="4235a-215">Select **Q#: Install command line project templates**</span></span>
   - <span data-ttu-id="4235a-216">Após alguns segundos, você verá um pop-up com a mensagem "Modelos de projeto instalados com êxito"</span><span class="sxs-lookup"><span data-stu-id="4235a-216">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>
