---
title: Desenvolver com Jupyter Notebooks do Q#
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 5c613d29c03525d29893307684f13ccd32d4d4eb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274017"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="76b1f-102">Desenvolver com Jupyter Notebooks do Q#</span><span class="sxs-lookup"><span data-stu-id="76b1f-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="76b1f-103">Instale o QDK para desenvolver operações Q# em Jupyter Notebooks do Q#.</span><span class="sxs-lookup"><span data-stu-id="76b1f-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="76b1f-104">Os Jupyter Notebooks permitem a execução de código in-loco juntamente com instruções, observações e outros tipos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="76b1f-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="76b1f-105">Esse ambiente é ideal para a escrita de código Q# com explicações inseridas ou tutoriais interativos de computação quântica.</span><span class="sxs-lookup"><span data-stu-id="76b1f-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="76b1f-106">Aqui está o que você precisa fazer para começar a criar seus próprios notebooks de Q#.</span><span class="sxs-lookup"><span data-stu-id="76b1f-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="76b1f-107">IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade principal para compilar e simular operações Q#.</span><span class="sxs-lookup"><span data-stu-id="76b1f-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="76b1f-108">Em Jupyter Notebooks do Q#, você só pode executar o código Q#, e as operações não podem ser chamadas em programas de host externos (por exemplo, arquivos do Python ou C#).</span><span class="sxs-lookup"><span data-stu-id="76b1f-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="76b1f-109">Esse ambiente não será apropriado se sua meta for combinar um programa de host clássico externo com o programa quântico.</span><span class="sxs-lookup"><span data-stu-id="76b1f-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="76b1f-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="76b1f-110">Prerequisites</span></span>

    - <span data-ttu-id="76b1f-111">[Python](https://www.python.org/downloads/) 3.6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="76b1f-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="76b1f-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="76b1f-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="76b1f-113">SDK do .NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="76b1f-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="76b1f-114">Instalar o pacote `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="76b1f-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="76b1f-115">Se você receber um erro durante a etapa `dotnet iqsharp install`, abra uma nova janela de terminal e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="76b1f-115">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="76b1f-116">Se isso ainda não funcionar, tente localizar a ferramenta `dotnet-iqsharp` instalada (no Windows, `dotnet-iqsharp.exe`) e executar:</span><span class="sxs-lookup"><span data-stu-id="76b1f-116">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="76b1f-117">em que `/path/to/dotnet-iqsharp` deverá ser substituída pelo caminho absoluto para a ferramenta `dotnet-iqsharp` no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="76b1f-117">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="76b1f-118">Normalmente, isso estará em `.dotnet/tools` na pasta de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="76b1f-118">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>

1. <span data-ttu-id="76b1f-119">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="76b1f-119">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="76b1f-120">Execute o seguinte comando para iniciar o servidor de notebook:</span><span class="sxs-lookup"><span data-stu-id="76b1f-120">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="76b1f-121">Para abrir o Jupyter Notebook, copie e cole a URL fornecida pela linha de comando no navegador.</span><span class="sxs-lookup"><span data-stu-id="76b1f-121">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="76b1f-122">Crie um Jupyter Notebook com um kernel do Q# e adicione o seguinte código à primeira célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="76b1f-122">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="76b1f-123">Execute esta célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="76b1f-123">Run this cell of the notebook:</span></span>

        ![Célula do Jupyter Notebook com o código Q#](~/media/install-guide-jupyter.png)

        <span data-ttu-id="76b1f-125">Você deverá ver `SayHello` na saída da célula.</span><span class="sxs-lookup"><span data-stu-id="76b1f-125">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="76b1f-126">Durante a execução no Jupyter Notebook, o código Q# é compilado e o notebook gera o nome das operações encontradas.</span><span class="sxs-lookup"><span data-stu-id="76b1f-126">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="76b1f-127">Em uma nova célula, execute a operação recém-criada (em um simulador) usando o comando `%simulate`:</span><span class="sxs-lookup"><span data-stu-id="76b1f-127">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Célula do Jupyter Notebook com o magic %simulate](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="76b1f-129">Você verá a mensagem impressa na tela junto com o resultado da operação invocada (aqui, vemos a tupla vazia `()` porque nossa operação apenas retorna um tipo `Unit`).</span><span class="sxs-lookup"><span data-stu-id="76b1f-129">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="76b1f-130">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="76b1f-130">Next steps</span></span>

<span data-ttu-id="76b1f-131">Agora que você instalou o QDK para Jupyter Notebooks do Q#, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng) escrevendo o código Q# diretamente no ambiente do Jupyter Notebook.</span><span class="sxs-lookup"><span data-stu-id="76b1f-131">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="76b1f-132">Para obter mais exemplos do que você pode fazer com Jupyter Notebooks do Q#, confira:</span><span class="sxs-lookup"><span data-stu-id="76b1f-132">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="76b1f-133">[Introdução ao Q# e ao Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="76b1f-133">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="76b1f-134">Nesse artigo, você encontrará um Jupyter Notebook do Q# que mostra como usar o Q# nesse ambiente.</span><span class="sxs-lookup"><span data-stu-id="76b1f-134">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="76b1f-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), uma coleção de software livre de tutoriais individuais e conjuntos de exercícios de programação na forma de Jupyter Notebooks do Q#.</span><span class="sxs-lookup"><span data-stu-id="76b1f-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="76b1f-136">Os [notebooks do tutorial do Quantum Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) são um bom ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="76b1f-136">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="76b1f-137">O Quantum Katas tem como objetivo ensinar elementos da computação quântica e programação com o Q# simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="76b1f-137">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="76b1f-138">Eles são um excelente exemplo do tipo de conteúdo que você pode criar com Jupyter Notebooks do Q#.</span><span class="sxs-lookup"><span data-stu-id="76b1f-138">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
