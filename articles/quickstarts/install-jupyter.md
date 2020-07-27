---
title: Desenvolver com Jupyter Notebooks do Q#
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: bbd1f58ba7de205e452be7bac72b5fd78e7acd56
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871443"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="67c79-102">Desenvolver com Jupyter Notebooks do Q#</span><span class="sxs-lookup"><span data-stu-id="67c79-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="67c79-103">Instale o QDK para desenvolver operações Q# em Jupyter Notebooks do Q#.</span><span class="sxs-lookup"><span data-stu-id="67c79-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="67c79-104">Os Jupyter Notebooks permitem a execução de código in-loco juntamente com instruções, observações e outros tipos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="67c79-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="67c79-105">Esse ambiente é ideal para a escrita de código Q# com explicações inseridas ou tutoriais interativos de computação quântica.</span><span class="sxs-lookup"><span data-stu-id="67c79-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="67c79-106">Aqui está o que você precisa fazer para começar a criar seus próprios notebooks de Q#.</span><span class="sxs-lookup"><span data-stu-id="67c79-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

> [!NOTE]
> * <span data-ttu-id="67c79-107">Com os Jupyter Notebooks do Q#, você pode executar somente código Q#, e as operações não podem ser chamadas de programas de host externos (por exemplo, de arquivos de Python ou C#).</span><span class="sxs-lookup"><span data-stu-id="67c79-107">In Q# Jupyter Notebooks, you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="67c79-108">Esse ambiente não será apropriado se sua meta for combinar um programa de host clássico externo com o programa quântico.</span><span class="sxs-lookup"><span data-stu-id="67c79-108">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

## <a name="install-the-iq-jupyter-kernel"></a><span data-ttu-id="67c79-109">Instalar o kernel de Jupyter do IQ#</span><span class="sxs-lookup"><span data-stu-id="67c79-109">Install the IQ# Jupyter kernel</span></span>

<span data-ttu-id="67c79-110">IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade principal para compilar e simular operações Q#.</span><span class="sxs-lookup"><span data-stu-id="67c79-110">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="67c79-111">Instalar usando o conda (recomendado)</span><span class="sxs-lookup"><span data-stu-id="67c79-111">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="67c79-112">Instale o [Miniconda](https://docs.conda.io/en/latest/miniconda.html) ou o [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span><span class="sxs-lookup"><span data-stu-id="67c79-112">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span> <span data-ttu-id="67c79-113">**Observação:** Instalação de 64 bits necessária.</span><span class="sxs-lookup"><span data-stu-id="67c79-113">**Note:** 64-bit installation required.</span></span>

1. <span data-ttu-id="67c79-114">Abra um prompt do Anaconda.</span><span class="sxs-lookup"><span data-stu-id="67c79-114">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="67c79-115">Ou, se preferir usar o PowerShell ou o pwsh: abra um shell, execute `conda init powershell` e feche-o e abra-o novamente.</span><span class="sxs-lookup"><span data-stu-id="67c79-115">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="67c79-116">Crie e ative um ambiente de conda chamado `qsharp-env` com os pacotes necessários (incluindo o Jupyter Notebook e o IQ#) executando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="67c79-116">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="67c79-117">Execute `python -c "import qsharp"` no mesmo terminal para confirmar a instalação e preencher o cache do pacote local com todos os componentes necessários do QDK.</span><span class="sxs-lookup"><span data-stu-id="67c79-117">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-advanced"></a>[<span data-ttu-id="67c79-118">Instalar usando a CLI do .NET (avançado)</span><span class="sxs-lookup"><span data-stu-id="67c79-118">Install using .NET CLI (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="67c79-119">Pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="67c79-119">Prerequisites:</span></span>

    - <span data-ttu-id="67c79-120">[Python](https://www.python.org/downloads/) 3.6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="67c79-120">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="67c79-121">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="67c79-121">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="67c79-122">SDK do .NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="67c79-122">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="67c79-123">Instale o pacote `Microsoft.Quantum.IQSharp`.</span><span class="sxs-lookup"><span data-stu-id="67c79-123">Install the `Microsoft.Quantum.IQSharp` package.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="67c79-124">Se você receber um erro durante a etapa `dotnet iqsharp install`, abra uma nova janela de terminal e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="67c79-124">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="67c79-125">Se isso ainda não funcionar, tente localizar a ferramenta `dotnet-iqsharp` instalada (no Windows, `dotnet-iqsharp.exe`) e executar:</span><span class="sxs-lookup"><span data-stu-id="67c79-125">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="67c79-126">em que `/path/to/dotnet-iqsharp` deverá ser substituída pelo caminho absoluto para a ferramenta `dotnet-iqsharp` no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="67c79-126">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="67c79-127">Normalmente, isso estará em `.dotnet/tools` na pasta de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="67c79-127">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
***

<span data-ttu-id="67c79-128">É isso!</span><span class="sxs-lookup"><span data-stu-id="67c79-128">That's it!</span></span> <span data-ttu-id="67c79-129">Agora, você tem o kernel do IQ# para Jupyter, que fornece a funcionalidade básica para compilar e executar operações de Q# nos Jupyter Notebooks do Q#.</span><span class="sxs-lookup"><span data-stu-id="67c79-129">You now have the IQ# kernel for Jupyter, which provides the core functionality for compiling and executing Q# operations from Q# Jupyter Notebooks.</span></span>

## <a name="create-your-first-q-notebook"></a><span data-ttu-id="67c79-130">Criar seu primeiro notebook em Q#</span><span class="sxs-lookup"><span data-stu-id="67c79-130">Create your first Q# notebook</span></span>

<span data-ttu-id="67c79-131">Agora, você pode verificar a instalação do Jupyter Notebook do Q# escrevendo e executando uma operação simples em Q#.</span><span class="sxs-lookup"><span data-stu-id="67c79-131">Now you are ready to verify your Q# Jupyter Notebook installation by writing and executing a simple Q# operation.</span></span>

1. <span data-ttu-id="67c79-132">No ambiente criado durante a instalação (ou seja, no ambiente de conda que você criou ou no ambiente de Python em que instalou o Jupyter), execute o seguinte comando para iniciar o servidor do Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="67c79-132">From the environment you created during installation (i.e., either the conda environment you created, or the Python environment where you installed Jupyter), run the following command to start the Jupyter Notebook server:</span></span>

    ```
    jupyter notebook
    ```

    - <span data-ttu-id="67c79-133">Se o Jupyter Notebook não abrir automaticamente no navegador, copie e cole a URL fornecida pela linha de comando no navegador.</span><span class="sxs-lookup"><span data-stu-id="67c79-133">If the Jupyter Notebook doesn't open automatically in your browser, copy and paste the URL provided by the command line into your browser.</span></span>

1. <span data-ttu-id="67c79-134">Escolha "Novo" → "Q#" para criar um Jupyter Notebook com um kernel do Q# e adicione o seguinte código à primeira célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="67c79-134">Choose "New" → "Q#" to create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="6-13":::

1. <span data-ttu-id="67c79-135">Execute esta célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="67c79-135">Run this cell of the notebook:</span></span>

    ![Célula do Jupyter Notebook com o código Q#](~/media/install-guide-jupyter.png)

    <span data-ttu-id="67c79-137">Você deverá ver `SampleQuantumRandomNumberGenerator` na saída da célula.</span><span class="sxs-lookup"><span data-stu-id="67c79-137">You should see `SampleQuantumRandomNumberGenerator` in the output of the cell.</span></span> <span data-ttu-id="67c79-138">Durante a execução no Jupyter Notebook, o código Q# é compilado e a célula gera o nome das operações encontradas.</span><span class="sxs-lookup"><span data-stu-id="67c79-138">When running in Jupyter Notebook, the Q# code is compiled, and the cell outputs the name of any operations that it finds.</span></span>

1. <span data-ttu-id="67c79-139">Em uma nova célula, execute a operação recém-criada (em um simulador) usando o comando `%simulate`:</span><span class="sxs-lookup"><span data-stu-id="67c79-139">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

    ![Célula do Jupyter Notebook com o magic %simulate](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="67c79-141">Você verá o resultado da operação que invocou.</span><span class="sxs-lookup"><span data-stu-id="67c79-141">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="67c79-142">Nesse caso, como a operação gera um resultado aleatório, você verá `Zero` ou `One` impresso na tela.</span><span class="sxs-lookup"><span data-stu-id="67c79-142">In this case, because your operation generates a random result, you will see either `Zero` or `One` printed on the screen.</span></span> <span data-ttu-id="67c79-143">Se executar a célula repetidamente, você verá cada resultado em aproximadamente metade do tempo.</span><span class="sxs-lookup"><span data-stu-id="67c79-143">If you execute the cell repeatedly, you should see each result approximately half the time.</span></span>

## <a name="next-steps"></a><span data-ttu-id="67c79-144">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="67c79-144">Next steps</span></span>

<span data-ttu-id="67c79-145">Agora que instalou o QDK para Jupyter Notebooks do Q#, você pode escrever e executar [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng) escrevendo o código Q# diretamente no ambiente do Jupyter Notebook.</span><span class="sxs-lookup"><span data-stu-id="67c79-145">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="67c79-146">Para obter mais exemplos do que você pode fazer com Jupyter Notebooks do Q#, confira:</span><span class="sxs-lookup"><span data-stu-id="67c79-146">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>

- <span data-ttu-id="67c79-147">[Introdução ao Q# e ao Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="67c79-147">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="67c79-148">Nesse artigo, há um Jupyter Notebook do Q# que fornece mais detalhes sobre como usar o Q# no ambiente do Jupyter.</span><span class="sxs-lookup"><span data-stu-id="67c79-148">There you will find a Q# Jupyter Notebook that provides more details on how to use Q# in the Jupyter environment.</span></span>
- <span data-ttu-id="67c79-149">[Quantum Katas](xref:microsoft.quantum.overview.katas), uma coleção de software livre de tutoriais individuais e conjuntos de exercícios de programação na forma de Jupyter Notebooks do Q#.</span><span class="sxs-lookup"><span data-stu-id="67c79-149">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="67c79-150">Os [notebooks do tutorial do Quantum Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) são um bom ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="67c79-150">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="67c79-151">O Quantum Katas tem como objetivo ensinar elementos da computação quântica e programação com o Q# simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="67c79-151">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="67c79-152">Eles são um excelente exemplo do tipo de conteúdo que você pode criar com Jupyter Notebooks do Q#.</span><span class="sxs-lookup"><span data-stu-id="67c79-152">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
