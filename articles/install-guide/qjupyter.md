---
title: Desenvolvimento com Jupyter Notebooks do Q#
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 9117794d6cf6f05fa34e05c21fad8977d0e76505
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84577813"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="9521a-102">Desenvolvimento com Jupyter Notebooks do Q#</span><span class="sxs-lookup"><span data-stu-id="9521a-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="9521a-103">Instale o QDK para desenvolver operações Q # em notebooks do Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="9521a-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="9521a-104">Os notebooks Jupyter permitem a execução de código in-loco juntamente com instruções, observações e outros conteúdos.</span><span class="sxs-lookup"><span data-stu-id="9521a-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="9521a-105">Esse ambiente é ideal para escrever código Q # com explicações incorporadas ou tutoriais interativos de computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="9521a-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="9521a-106">Aqui está o que você precisa fazer para começar a criar seus próprios notebooks de Q#.</span><span class="sxs-lookup"><span data-stu-id="9521a-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="9521a-107">IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade principal para compilar e simular operações Q#.</span><span class="sxs-lookup"><span data-stu-id="9521a-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="9521a-108">Em Jupyter notebooks do Q #, você só pode executar o código Q # e as operações não podem ser chamadas de programas de host externos (por exemplo, arquivos Python ou C#).</span><span class="sxs-lookup"><span data-stu-id="9521a-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="9521a-109">Esse ambiente não será apropriado se o seu objetivo for combinar um programa host clássico externo com o programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="9521a-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="9521a-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9521a-110">Pre-requisites</span></span>

    - <span data-ttu-id="9521a-111">[Python](https://www.python.org/downloads/) 3,6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9521a-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="9521a-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="9521a-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="9521a-113">SDK do .NET Core 3,1</span><span class="sxs-lookup"><span data-stu-id="9521a-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="9521a-114">Instalar o pacote `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="9521a-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="9521a-115">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="9521a-115">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="9521a-116">Execute o seguinte comando para iniciar o servidor de notebook:</span><span class="sxs-lookup"><span data-stu-id="9521a-116">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="9521a-117">Para abrir o Jupyter Notebook, copie e cole a URL fornecida pela linha de comando em seu navegador.</span><span class="sxs-lookup"><span data-stu-id="9521a-117">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="9521a-118">Crie um Jupyter Notebook com um kernel Q # e adicione o seguinte código à primeira célula do bloco de anotações:</span><span class="sxs-lookup"><span data-stu-id="9521a-118">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="9521a-119">Execute esta célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="9521a-119">Run this cell of the notebook:</span></span>

        ![Jupyter Notebook célula com código Q #](~/media/install-guide-jupyter.png)

        <span data-ttu-id="9521a-121">Você deverá ver `SayHello` na saída da célula.</span><span class="sxs-lookup"><span data-stu-id="9521a-121">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="9521a-122">Quando executado no Jupyter Notebook, o código Q # é compilado e o notebook gera o nome da (s) operação (ões) que encontrar.</span><span class="sxs-lookup"><span data-stu-id="9521a-122">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="9521a-123">Em uma nova célula, execute a operação que você acabou de criar (em um simulador) usando o `%simulate` comando:</span><span class="sxs-lookup"><span data-stu-id="9521a-123">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Jupyter Notebook célula com% simula mágica](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="9521a-125">Você deve ver a mensagem impressa na tela junto com o resultado da operação que você chamou (aqui, vemos a tupla vazia `()` porque nossa operação simplesmente retorna um `Unit` tipo).</span><span class="sxs-lookup"><span data-stu-id="9521a-125">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="9521a-126">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9521a-126">Next steps</span></span>

<span data-ttu-id="9521a-127">Agora que você instalou o QDK para os notebooks do Q # Jupyter, você pode escrever e executar [seu primeiro programa Quantum](xref:microsoft.quantum.quickstarts.qrng) escrevendo o código de q # diretamente no ambiente de Jupyter notebook.</span><span class="sxs-lookup"><span data-stu-id="9521a-127">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="9521a-128">Para obter mais exemplos do que você pode fazer com o Q # Jupyter notebooks, consulte:</span><span class="sxs-lookup"><span data-stu-id="9521a-128">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="9521a-129">[Introdução à Q # e Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="9521a-129">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="9521a-130">Lá, você encontrará um Jupyter Notebook Q # que mostra como usar o Q # nesse ambiente.</span><span class="sxs-lookup"><span data-stu-id="9521a-130">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="9521a-131">[Quantum katas](xref:microsoft.quantum.overview.katas), uma coleção de código aberto de tutoriais individualizados e conjuntos de exercícios de programação na forma de Jupyter notebooks de Q #.</span><span class="sxs-lookup"><span data-stu-id="9521a-131">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="9521a-132">Os [notebooks do tutorial Katas do Quantum](https://github.com/microsoft/QuantumKatas#tutorial-topics) são um bom ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="9521a-132">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="9521a-133">O Quantum katas tem como objetivo ensinar os elementos de computação Quantum e a programação Q # ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9521a-133">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="9521a-134">Eles são um excelente exemplo do tipo de conteúdo que você pode criar com os notebooks Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="9521a-134">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
