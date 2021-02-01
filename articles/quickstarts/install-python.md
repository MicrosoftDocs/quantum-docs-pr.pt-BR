---
title: Desenvolver com o Q# e o Python
description: Saiba como criar um aplicativo Q# usando o Python.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.python
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1ec40b6f1b7a8d9144860e3b8cfd554eb51bae81
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844264"
---
# <a name="develop-with-no-locq-and-python"></a><span data-ttu-id="7cfaf-103">Desenvolver com o Q# e o Python</span><span class="sxs-lookup"><span data-stu-id="7cfaf-103">Develop with Q# and Python</span></span>

<span data-ttu-id="7cfaf-104">Instale o QDK para desenvolver programas de host do Python para chamar operações Q#.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-104">Install the QDK to develop Python host programs to call Q# operations.</span></span>

## <a name="install-the-qsharp-python-package"></a><span data-ttu-id="7cfaf-105">Instalar o pacote `qsharp` do Python</span><span class="sxs-lookup"><span data-stu-id="7cfaf-105">Install the `qsharp` Python package</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="7cfaf-106">Instalar usando o conda (recomendado)</span><span class="sxs-lookup"><span data-stu-id="7cfaf-106">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="7cfaf-107">Instale o [Miniconda](https://docs.conda.io/en/latest/miniconda.html) ou o [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span><span class="sxs-lookup"><span data-stu-id="7cfaf-107">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span> <span data-ttu-id="7cfaf-108">**Observação:** Instalação de 64 bits necessária.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-108">**Note:** 64-bit installation required.</span></span>

1. <span data-ttu-id="7cfaf-109">Abra um prompt do Anaconda.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-109">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="7cfaf-110">Ou, se preferir usar o PowerShell ou o pwsh: abra um shell, execute `conda init powershell` e feche-o e abra-o novamente.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-110">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="7cfaf-111">Crie e ative um novo ambiente de conda chamado `qsharp-env` com os pacotes necessários (incluindo o Jupyter Notebook e o IQ#) executando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="7cfaf-111">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="7cfaf-112">Execute `python -c "import qsharp"` no mesmo terminal para confirmar a instalação e preencher o cache do pacote local com todos os componentes necessários do QDK.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-112">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="7cfaf-113">Instalar usando a CLI do .NET e o pip (avançado)</span><span class="sxs-lookup"><span data-stu-id="7cfaf-113">Install using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="7cfaf-114">Pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="7cfaf-114">Prerequisites:</span></span>

    - <span data-ttu-id="7cfaf-115">[Python](https://www.python.org/downloads/) 3.6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7cfaf-115">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="7cfaf-116">O gerenciador de pacotes Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="7cfaf-116">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="7cfaf-117">SDK do .NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="7cfaf-117">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="7cfaf-118">Instale o pacote `qsharp`, um pacote do Python que permite a interoperabilidade entre o Q# e o Python.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-118">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="7cfaf-119">Instale o IQ#, um kernel usado pelo Jupyter e pelo Python que fornece uma funcionalidade básica para compilar e executar operações Q#.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-119">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and running Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="7cfaf-120">Se você receber um erro durante a etapa `dotnet iqsharp install`, abra uma nova janela de terminal e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-120">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="7cfaf-121">Se isso ainda não funcionar, tente localizar a ferramenta `dotnet-iqsharp` instalada (no Windows, `dotnet-iqsharp.exe`) e executar:</span><span class="sxs-lookup"><span data-stu-id="7cfaf-121">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="7cfaf-122">em que `/path/to/dotnet-iqsharp` deverá ser substituída pelo caminho absoluto para a ferramenta `dotnet-iqsharp` no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-122">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="7cfaf-123">Normalmente, isso estará em `.dotnet/tools` na pasta de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-123">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
<span data-ttu-id="7cfaf-124">\*\*_</span><span class="sxs-lookup"><span data-stu-id="7cfaf-124">\*\*_</span></span>

<span data-ttu-id="7cfaf-125">É isso!</span><span class="sxs-lookup"><span data-stu-id="7cfaf-125">That's it!</span></span> <span data-ttu-id="7cfaf-126">Agora você tem o pacote `qsharp` do Python e o kernel do IQ# para Jupyter, que fornecem uma funcionalidade básica para compilar e executar operações Q# do Python e permite usar Jupyter Notebooks do Q#.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-126">You now have both the `qsharp` Python package and the IQ# kernel for Jupyter, which provide the core functionality for compiling and running Q# operations from Python and allows you to use Q# Jupyter Notebooks.</span></span>

## <a name="choose-your-ide"></a><span data-ttu-id="7cfaf-127">Escolher o IDE</span><span class="sxs-lookup"><span data-stu-id="7cfaf-127">Choose your IDE</span></span>

<span data-ttu-id="7cfaf-128">Embora seja possível usar o Q# com o Python em qualquer IDE, é bastante recomendável usar o IDE do VS Code (Visual Studio Code) para os aplicativos Q# + Python.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-128">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="7cfaf-129">Com a extensão do Visual Studio Code para o QDK, você tem acesso a funcionalidades mais sofisticadas, como avisos, realce de sintaxe, modelos de projeto e muito mais.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-129">With the QDK Visual Studio Code extension you gain access to richer functionality such as warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="7cfaf-130">Se quiser usar o VS Code:</span><span class="sxs-lookup"><span data-stu-id="7cfaf-130">If you would like to use VS Code:</span></span>

- <span data-ttu-id="7cfaf-131">Instale o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).</span><span class="sxs-lookup"><span data-stu-id="7cfaf-131">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
- <span data-ttu-id="7cfaf-132">Instale a [extensão do QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="7cfaf-132">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="7cfaf-133">Se você prefere usar outro editor, as instruções acima fornecem todas as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-133">If you would like to use a different editor, the instructions above have you all set.</span></span>

## <a name="write-your-first-no-locq-program"></a><span data-ttu-id="7cfaf-134">Escrever seu primeiro programa Q#</span><span class="sxs-lookup"><span data-stu-id="7cfaf-134">Write your first Q# program</span></span>

<span data-ttu-id="7cfaf-135">Agora você está pronto para verificar a instalação do pacote `qsharp` do Python gravando e executando um programa de Q# simples.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-135">Now you are ready to verify your `qsharp` Python package installation by writing and running a simple Q# program.</span></span>

1. <span data-ttu-id="7cfaf-136">Crie uma operação mínima de Q# criando um arquivo chamado `Operation.qs` e adicionando o seguinte código a ele:</span><span class="sxs-lookup"><span data-stu-id="7cfaf-136">Create a minimal Q# operation by creating a file called `Operation.qs` and adding the following code to it:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. <span data-ttu-id="7cfaf-137">Na mesma pasta de `Operation.qs`, crie um programa Python chamado `host.py` para simular a operação Q# `SampleQuantumRandomNumberGenerator()`:</span><span class="sxs-lookup"><span data-stu-id="7cfaf-137">In the same folder as `Operation.qs`, create a Python program called `host.py` to simulate the Q# `SampleQuantumRandomNumberGenerator()` operation:</span></span>

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    print(SampleQuantumRandomNumberGenerator.simulate())
    ```

1. <span data-ttu-id="7cfaf-138">No ambiente criado durante a instalação (ou seja, o ambiente de conda ou de Python em que você instalou `qsharp`), execute o programa:</span><span class="sxs-lookup"><span data-stu-id="7cfaf-138">From the environment you created during installation (i.e., the conda or Python environment where you installed `qsharp`), run the program:</span></span>

    ```
    python host.py
    ```

1. <span data-ttu-id="7cfaf-139">Você verá o resultado da operação que invocou.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-139">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="7cfaf-140">Nesse caso, como a operação gera um resultado aleatório, você verá `0` ou `1` impresso na tela.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-140">In this case, because your operation generates a random result, you will see either `0` or `1` printed on the screen.</span></span> <span data-ttu-id="7cfaf-141">Caso execute o programa várias vezes, será possível conferir cada resultado em aproximadamente metade do tempo.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-141">If you run the program repeatedly, you should see each result approximately half the time.</span></span>

> [!NOTE]
> <span data-ttu-id="7cfaf-142">_ O código Python é apenas um programa Python normal.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-142">_ The Python code is just a normal Python program.</span></span> <span data-ttu-id="7cfaf-143">É possível usar qualquer ambiente Python, incluindo Jupyter Notebooks baseados em Python, para escrever o programa nessa linguagem de programação e chamar as operações Q#.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-143">You can use any Python environment, including Python-based Jupyter Notebooks, to write the Python program and call Q# operations.</span></span> <span data-ttu-id="7cfaf-144">O programa Python pode importar operações de Q# de arquivos .qs localizados na mesma pasta que o código Python.</span><span class="sxs-lookup"><span data-stu-id="7cfaf-144">The Python program can import Q# operations from any .qs files located in the same folder as the Python code itself.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7cfaf-145">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="7cfaf-145">Next steps</span></span>

<span data-ttu-id="7cfaf-146">Agora que você testou o Kit de Desenvolvimento Quantum em um ambiente preferencial, será possível seguir este tutorial para gravar e executar [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="7cfaf-146">Now that you have tested the Quantum Development Kit in your preferred environment, you can follow this tutorial to write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
