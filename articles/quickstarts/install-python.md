---
title: Desenvolver com o Q# e o Python
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 7fbbb81b1ee51bff74b287745bf4447004a0254c
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885535"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="3261b-102">Desenvolver com o Q# e o Python</span><span class="sxs-lookup"><span data-stu-id="3261b-102">Develop with Q# and Python</span></span>

<span data-ttu-id="3261b-103">Instale o QDK para desenvolver programas de host do Python para chamar operações Q#.</span><span class="sxs-lookup"><span data-stu-id="3261b-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

## <a name="install-the-qsharp-python-package"></a><span data-ttu-id="3261b-104">Instalar o pacote `qsharp` do Python</span><span class="sxs-lookup"><span data-stu-id="3261b-104">Install the `qsharp` Python package</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="3261b-105">Instalar usando o conda (recomendado)</span><span class="sxs-lookup"><span data-stu-id="3261b-105">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="3261b-106">Instale o [Miniconda](https://docs.conda.io/en/latest/miniconda.html) ou o [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span><span class="sxs-lookup"><span data-stu-id="3261b-106">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span>

1. <span data-ttu-id="3261b-107">Abra um prompt do Anaconda.</span><span class="sxs-lookup"><span data-stu-id="3261b-107">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="3261b-108">Ou, se preferir usar o PowerShell ou o pwsh: abra um shell, execute `conda init powershell` e feche-o e abra-o novamente.</span><span class="sxs-lookup"><span data-stu-id="3261b-108">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="3261b-109">Crie e ative um ambiente de conda chamado `qsharp-env` com os pacotes necessários (incluindo o Jupyter Notebook e o IQ#) executando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="3261b-109">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="3261b-110">Execute `python -c "import qsharp"` no mesmo terminal para confirmar a instalação e preencher o cache do pacote local com todos os componentes necessários do QDK.</span><span class="sxs-lookup"><span data-stu-id="3261b-110">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="3261b-111">Instalar usando a CLI do .NET e o pip (avançado)</span><span class="sxs-lookup"><span data-stu-id="3261b-111">Install using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="3261b-112">Pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="3261b-112">Prerequisites:</span></span>

    - <span data-ttu-id="3261b-113">[Python](https://www.python.org/downloads/) 3.6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3261b-113">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="3261b-114">O gerenciador de pacotes Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="3261b-114">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="3261b-115">SDK do .NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="3261b-115">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="3261b-116">Instale o pacote `qsharp`, um pacote do Python que permite a interoperabilidade entre o Q# e o Python.</span><span class="sxs-lookup"><span data-stu-id="3261b-116">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="3261b-117">Instale o IQ#, um kernel usado pelo Jupyter e pelo Python que fornece a funcionalidade básica para compilar e executar operações Q#.</span><span class="sxs-lookup"><span data-stu-id="3261b-117">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="3261b-118">Se você receber um erro durante a etapa `dotnet iqsharp install`, abra uma nova janela de terminal e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="3261b-118">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="3261b-119">Se isso ainda não funcionar, tente localizar a ferramenta `dotnet-iqsharp` instalada (no Windows, `dotnet-iqsharp.exe`) e executar:</span><span class="sxs-lookup"><span data-stu-id="3261b-119">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="3261b-120">em que `/path/to/dotnet-iqsharp` deverá ser substituída pelo caminho absoluto para a ferramenta `dotnet-iqsharp` no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3261b-120">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="3261b-121">Normalmente, isso estará em `.dotnet/tools` na pasta de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="3261b-121">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
***

<span data-ttu-id="3261b-122">É isso!</span><span class="sxs-lookup"><span data-stu-id="3261b-122">That's it!</span></span> <span data-ttu-id="3261b-123">Agora, você tem o pacote `qsharp` do Python e o kernel do IQ# para Jupyter, que fornece a funcionalidade básica para compilar e executar operações de Q# no Python e permite usar os Jupyter Notebooks do Q#.</span><span class="sxs-lookup"><span data-stu-id="3261b-123">You now have both the `qsharp` Python package and the IQ# kernel for Jupyter, which provides the core functionality for compiling and executing Q# operations from Python and allows you to use Q# Jupyter Notebooks.</span></span>

## <a name="choose-your-ide"></a><span data-ttu-id="3261b-124">Escolher o IDE</span><span class="sxs-lookup"><span data-stu-id="3261b-124">Choose your IDE</span></span>

<span data-ttu-id="3261b-125">Embora você possa usar o Q# com o Python em qualquer IDE, recomendamos expressamente usar o IDE do VS Code (Visual Studio Code) para seus aplicativos Q# + Python.</span><span class="sxs-lookup"><span data-stu-id="3261b-125">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="3261b-126">Com a extensão do Visual Studio Code para o QDK, você tem acesso a funcionalidades mais sofisticadas, como avisos, realce de sintaxe, modelos de projeto e muito mais.</span><span class="sxs-lookup"><span data-stu-id="3261b-126">With the QDK Visual Studio Code extension you gain access to richer functionality such as warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="3261b-127">Se quiser usar o VS Code:</span><span class="sxs-lookup"><span data-stu-id="3261b-127">If you would like to use VS Code:</span></span>

- <span data-ttu-id="3261b-128">Instale o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).</span><span class="sxs-lookup"><span data-stu-id="3261b-128">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
- <span data-ttu-id="3261b-129">Instale a [extensão do QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="3261b-129">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="3261b-130">Se você prefere usar outro editor, as instruções acima fornecem todas as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="3261b-130">If you would like to use a different editor, the instructions above have you all set.</span></span>

## <a name="write-your-first-q-program"></a><span data-ttu-id="3261b-131">Escrever seu primeiro programa em Q#</span><span class="sxs-lookup"><span data-stu-id="3261b-131">Write your first Q# program</span></span>

<span data-ttu-id="3261b-132">Agora, você pode verificar a instalação do pacote `qsharp` do Python escrevendo e executando um programa simples em Q#.</span><span class="sxs-lookup"><span data-stu-id="3261b-132">Now you are ready to verify your `qsharp` Python package installation by writing and executing a simple Q# program.</span></span>

1. <span data-ttu-id="3261b-133">Crie uma operação de Q# mínima criando um arquivo chamado `Operation.qs` e adicionando o seguinte código a ele:</span><span class="sxs-lookup"><span data-stu-id="3261b-133">Create a minimal Q# operation by creating a file called `Operation.qs` and adding the following code to it:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. <span data-ttu-id="3261b-134">Na mesma pasta que `Operation.qs`, crie um programa de Python chamado `host.py` para simular a operação `SampleQuantumRandomNumberGenerator()` de Q#:</span><span class="sxs-lookup"><span data-stu-id="3261b-134">In the same folder as `Operation.qs`, create a Python program called `host.py` to simulate the Q# `SampleQuantumRandomNumberGenerator()` operation:</span></span>

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    SampleQuantumRandomNumberGenerator.simulate()
    ```

1. <span data-ttu-id="3261b-135">No ambiente criado durante a instalação (ou seja, o ambiente de conda ou de Python em que você instalou `qsharp`), execute o programa:</span><span class="sxs-lookup"><span data-stu-id="3261b-135">From the environment you created during installation (i.e., the conda or Python environment where you installed `qsharp`), run the program:</span></span>

    ```
    python host.py
    ```

1. <span data-ttu-id="3261b-136">Você verá o resultado da operação que invocou.</span><span class="sxs-lookup"><span data-stu-id="3261b-136">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="3261b-137">Nesse caso, como a operação gera um resultado aleatório, você verá `Zero` ou `One` impresso na tela.</span><span class="sxs-lookup"><span data-stu-id="3261b-137">In this case, because your operation generates a random result, you will see either `Zero` or `One` printed on the screen.</span></span> <span data-ttu-id="3261b-138">Se executar o programa repetidamente, você verá cada resultado em aproximadamente metade do tempo.</span><span class="sxs-lookup"><span data-stu-id="3261b-138">If you execute the program repeatedly, you should see each result approximately half the time.</span></span>

> [!NOTE]
> * <span data-ttu-id="3261b-139">O código Python é apenas um programa Python normal.</span><span class="sxs-lookup"><span data-stu-id="3261b-139">The Python code is just a normal Python program.</span></span> <span data-ttu-id="3261b-140">Você pode usar qualquer ambiente de Python, incluindo Jupyter Notebooks baseados em Python, para escrever o programa nessa linguagem de programação e chamar as operações de Q#.</span><span class="sxs-lookup"><span data-stu-id="3261b-140">You can use any Python environment, including Python-based Jupyter Notebooks, to write the Python program and call Q# operations.</span></span> <span data-ttu-id="3261b-141">O programa em Python pode importar operações de Q# de arquivos .qs localizados na mesma pasta que o código Python.</span><span class="sxs-lookup"><span data-stu-id="3261b-141">The Python program can import Q# operations from any .qs files located in the same folder as the Python code itself.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3261b-142">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="3261b-142">Next steps</span></span>

<span data-ttu-id="3261b-143">Agora que você instalou o Quantum Development Kit em seu ambiente preferido, siga este tutorial para escrever e executar [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="3261b-143">Now that you have installed the Quantum Development Kit in your preferred environment, you can follow this tutorial to write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
