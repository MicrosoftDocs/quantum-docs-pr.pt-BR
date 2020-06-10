---
title: Desenvolvimento com Jupyter Notebooks do Q#
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b80d95a160b5f46c1132d3428ba32ad6dcd5656e
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630341"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="0fcc1-102">Desenvolvimento com Jupyter Notebooks do Q#</span><span class="sxs-lookup"><span data-stu-id="0fcc1-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="0fcc1-103">Instale o QDK para desenvolver operações Q # em notebooks do Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="0fcc1-104">Os notebooks Jupyter permitem a execução de código in-loco juntamente com instruções, observações e outros conteúdos.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="0fcc1-105">Esse ambiente é ideal para escrever código Q # com explicações incorporadas ou tutoriais interativos de computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="0fcc1-106">Aqui está o que você precisa fazer para começar a criar seus próprios notebooks de Q#.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="0fcc1-107">IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade principal para compilar e simular operações Q#.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="0fcc1-108">Em Jupyter notebooks do Q #, você só pode executar o código Q # e as operações não podem ser chamadas de programas de host externos (por exemplo, arquivos Python ou C#).</span><span class="sxs-lookup"><span data-stu-id="0fcc1-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="0fcc1-109">Esse ambiente não será apropriado se o seu objetivo for combinar um programa host clássico externo com o programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="0fcc1-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="0fcc1-110">Prerequisites</span></span>

    - <span data-ttu-id="0fcc1-111">[Python](https://www.python.org/downloads/) 3,6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0fcc1-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="0fcc1-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="0fcc1-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="0fcc1-113">SDK do .NET Core 3,1</span><span class="sxs-lookup"><span data-stu-id="0fcc1-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="0fcc1-114">Instalar o pacote `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="0fcc1-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="0fcc1-115">Se você receber um erro durante a `dotnet iqsharp install` etapa, abra uma nova janela do terminal e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-115">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="0fcc1-116">Se isso ainda não funcionar, tente localizar a `dotnet-iqsharp` ferramenta instalada (no Windows `dotnet-iqsharp.exe` ) e executar:</span><span class="sxs-lookup"><span data-stu-id="0fcc1-116">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="0fcc1-117">onde `/path/to/dotnet-iqsharp` o deve ser substituído pelo caminho absoluto para a `dotnet-iqsharp` ferramenta no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-117">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="0fcc1-118">Normalmente, isso estará em `.dotnet/tools` na sua pasta de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-118">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>

1. <span data-ttu-id="0fcc1-119">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="0fcc1-119">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="0fcc1-120">Execute o seguinte comando para iniciar o servidor de notebook:</span><span class="sxs-lookup"><span data-stu-id="0fcc1-120">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="0fcc1-121">Para abrir o Jupyter Notebook, copie e cole a URL fornecida pela linha de comando em seu navegador.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-121">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="0fcc1-122">Crie um Jupyter Notebook com um kernel Q # e adicione o seguinte código à primeira célula do bloco de anotações:</span><span class="sxs-lookup"><span data-stu-id="0fcc1-122">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="0fcc1-123">Execute esta célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="0fcc1-123">Run this cell of the notebook:</span></span>

        ![Jupyter Notebook célula com código Q #](~/media/install-guide-jupyter.png)

        <span data-ttu-id="0fcc1-125">Você deverá ver `SayHello` na saída da célula.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-125">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="0fcc1-126">Quando executado no Jupyter Notebook, o código Q # é compilado e o notebook gera o nome da (s) operação (ões) que encontrar.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-126">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="0fcc1-127">Em uma nova célula, execute a operação que você acabou de criar (em um simulador) usando o `%simulate` comando:</span><span class="sxs-lookup"><span data-stu-id="0fcc1-127">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Jupyter Notebook célula com% simula mágica](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="0fcc1-129">Você deve ver a mensagem impressa na tela junto com o resultado da operação que você chamou (aqui, vemos a tupla vazia `()` porque nossa operação simplesmente retorna um `Unit` tipo).</span><span class="sxs-lookup"><span data-stu-id="0fcc1-129">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="0fcc1-130">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="0fcc1-130">Next steps</span></span>

<span data-ttu-id="0fcc1-131">Agora que você instalou o QDK para os notebooks do Q # Jupyter, você pode escrever e executar [seu primeiro programa Quantum](xref:microsoft.quantum.quickstarts.qrng) escrevendo o código de q # diretamente no ambiente de Jupyter notebook.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-131">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="0fcc1-132">Para obter mais exemplos do que você pode fazer com o Q # Jupyter notebooks, consulte:</span><span class="sxs-lookup"><span data-stu-id="0fcc1-132">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="0fcc1-133">[Introdução à Q # e Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="0fcc1-133">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="0fcc1-134">Lá, você encontrará um Jupyter Notebook Q # que mostra como usar o Q # nesse ambiente.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-134">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="0fcc1-135">[Quantum katas](xref:microsoft.quantum.overview.katas), uma coleção de código aberto de tutoriais individualizados e conjuntos de exercícios de programação na forma de Jupyter notebooks de Q #.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="0fcc1-136">Os [notebooks do tutorial Katas do Quantum](https://github.com/microsoft/QuantumKatas#tutorial-topics) são um bom ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-136">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="0fcc1-137">O Quantum katas tem como objetivo ensinar os elementos de computação Quantum e a programação Q # ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-137">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="0fcc1-138">Eles são um excelente exemplo do tipo de conteúdo que você pode criar com os notebooks Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="0fcc1-138">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
