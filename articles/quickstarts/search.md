---
title: Executar o algoritmo de pesquisa de Grover em Q# – Quantum development kit
description: Crie um projeto Q# que demonstra o algoritmo de Grover, um dos algoritmos quânticos canônicos.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: c1fd578fdb3d56a7b48972e6ccc9b1605047fe36
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820344"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="6fb58-103">Início Rápido: Implementar o algoritmo de pesquisa de Grover em Q#</span><span class="sxs-lookup"><span data-stu-id="6fb58-103">Quickstart: Implement Grover's search algorithm in Q#</span></span>

<span data-ttu-id="6fb58-104">Neste Início Rápido, você pode aprender a criar e executar a pesquisa de Grover para acelerar a pesquisa de dados não estruturados.</span><span class="sxs-lookup"><span data-stu-id="6fb58-104">In this Quickstart, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="6fb58-105">A pesquisa de Grover é um dos algoritmos de computação quântica mais populares e essa implementação do Q# relativamente pequena dá uma noção das vantagens da programação de soluções quânticas com uma linguagem de programação quântica Q# de alto nível para expressar algoritmos quânticos.</span><span class="sxs-lookup"><span data-stu-id="6fb58-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="6fb58-106">No fim do guia, você verá que a saída da simulação demonstra com êxito a localização de uma cadeia de caracteres específica entre uma lista de entradas não ordenadas em uma fração do tempo que levaria para pesquisar toda a lista em um computador clássico.</span><span class="sxs-lookup"><span data-stu-id="6fb58-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of onordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="6fb58-107">O algoritmo de Grover pesquisa itens específicos em uma lista de dados não estruturados.</span><span class="sxs-lookup"><span data-stu-id="6fb58-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="6fb58-108">Por exemplo, ele pode responder à pergunta: Esta carta retirada de um baralho é um ás de copas?</span><span class="sxs-lookup"><span data-stu-id="6fb58-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="6fb58-109">A rotulagem do item específico é chamada _entrada marcada_.</span><span class="sxs-lookup"><span data-stu-id="6fb58-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="6fb58-110">Usando o algoritmo de pesquisa de Grover, é garantido que um computador quântico execute essa pesquisa em menos etapas do que o número de itens na lista que você está pesquisando – algo que nenhum algoritmo clássico pode fazer.</span><span class="sxs-lookup"><span data-stu-id="6fb58-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="6fb58-111">A maior velocidade no caso de um baralho é insignificante; no entanto, em listas que contêm milhões ou bilhões de itens, ela se torna significativa.</span><span class="sxs-lookup"><span data-stu-id="6fb58-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="6fb58-112">Você pode criar o algoritmo de pesquisa de Grover com apenas algumas linhas de código.</span><span class="sxs-lookup"><span data-stu-id="6fb58-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6fb58-113">Prerequisites</span><span class="sxs-lookup"><span data-stu-id="6fb58-113">Prerequisites</span></span>

- <span data-ttu-id="6fb58-114">O Microsoft [Quantum development kit][install].</span><span class="sxs-lookup"><span data-stu-id="6fb58-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="6fb58-115">O que o algoritmo de pesquisa de Grover faz?</span><span class="sxs-lookup"><span data-stu-id="6fb58-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="6fb58-116">O algoritmo de Grover pergunta se um item de uma lista é aquele que estamos procurando.</span><span class="sxs-lookup"><span data-stu-id="6fb58-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="6fb58-117">Ele faz isso construindo uma superposição quântica dos índices da lista com cada coeficiente, ou amplitude de probabilidade, representando a probabilidade desse índice específico ser aquele que você está procurando.</span><span class="sxs-lookup"><span data-stu-id="6fb58-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="6fb58-118">No centro do algoritmo há duas etapas que aumentam de maneira incremental o coeficiente do índice que estamos procurando, até a amplitude da probabilidade desse coeficiente se aproximar de um.</span><span class="sxs-lookup"><span data-stu-id="6fb58-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="6fb58-119">O número de aumentos incrementais é menor que o número de itens na lista.</span><span class="sxs-lookup"><span data-stu-id="6fb58-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="6fb58-120">É por isso que o algoritmo de pesquisa de Grover executa a pesquisa em menos etapas do que qualquer algoritmo clássico.</span><span class="sxs-lookup"><span data-stu-id="6fb58-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Diagrama funcional do algoritmo de pesquisa de Grover](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="6fb58-122">Escreva o código</span><span class="sxs-lookup"><span data-stu-id="6fb58-122">Write the code</span></span>

1. <span data-ttu-id="6fb58-123">Usando o Quantum development kit, [crie um projeto Q#](xref:microsoft.quantum.howto.createproject) chamado `Grover` no ambiente de desenvolvimento de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="6fb58-123">Using the Quantum Development Kit, [create a new Q# project](xref:microsoft.quantum.howto.createproject) called `Grover`, in your development environment of choice.</span></span>

1. <span data-ttu-id="6fb58-124">Adicione o seguinte código ao arquivo `Operations.qs` no novo projeto:</span><span class="sxs-lookup"><span data-stu-id="6fb58-124">Add the following code to the `Operations.qs` file in your new project:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-23" highlight="5,27":::

1. <span data-ttu-id="6fb58-125">Para definir a lista que estamos pesquisando, crie um arquivo `Reflections.qs` e cole o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="6fb58-125">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    <span data-ttu-id="6fb58-126">A operação `ReflectAboutMarked` define a entrada marcada que você está pesquisando: a cadeia de caracteres que alterna zeros e uns.</span><span class="sxs-lookup"><span data-stu-id="6fb58-126">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="6fb58-127">Essa amostra embute a entrada marcada em código e pode ser estendida para pesquisar diferentes entradas ou generalizada para qualquer entrada.</span><span class="sxs-lookup"><span data-stu-id="6fb58-127">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="6fb58-128">Em seguida, execute o novo programa Q# para encontrar o item marcado por `ReflectAboutMarked`.</span><span class="sxs-lookup"><span data-stu-id="6fb58-128">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-linetabtabid-python"></a>[<span data-ttu-id="6fb58-129">Python com Visual Studio Code ou a linha de comando</span><span class="sxs-lookup"><span data-stu-id="6fb58-129">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="6fb58-130">Para executar o novo programa Q# no Python, salve o seguinte código como `host.py`:</span><span class="sxs-lookup"><span data-stu-id="6fb58-130">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

    :::code language="python" source="~/quantum/samples/algorithms/simple-grover/host.py" range="9-14":::

    <span data-ttu-id="6fb58-131">Em seguida, execute o programa host do Python na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="6fb58-131">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    [0, 1, 0, 1, 0]
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-linetabtabid-csharp"></a>[<span data-ttu-id="6fb58-132">C# com Visual Studio Code ou a linha de comando</span><span class="sxs-lookup"><span data-stu-id="6fb58-132">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="6fb58-133">Para executar o novo programa Q# no C#, modifique `Driver.cs` para incluir o seguinte código C#:</span><span class="sxs-lookup"><span data-stu-id="6fb58-133">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    <span data-ttu-id="6fb58-134">Em seguida, execute o programa host do C# na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="6fb58-134">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```

    ### <a name="c-with-visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="6fb58-135">C# com Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="6fb58-135">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="6fb58-136">Para executar seu novo programa em Q# no C# no Visual Studio, modifique `Driver.cs` para incluir o seguinte código C#:</span><span class="sxs-lookup"><span data-stu-id="6fb58-136">To run your new Q# program from C# in Visual Studio, modify `Driver.cs` to include the following C# code:</span></span>

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    <span data-ttu-id="6fb58-137">Em seguida, pressione F5. O programa iniciará a execução e uma nova janela será exibida com os seguintes resultados:</span><span class="sxs-lookup"><span data-stu-id="6fb58-137">Then press F5, the program will start execution and a new windows will pop-up with the following results:</span></span> 

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```
    ***

    <span data-ttu-id="6fb58-138">A operação `ReflectAboutMarked` é chamada apenas quatro vezes, mas o programa Q# conseguiu encontrar a entrada "01010" entre $2^{5} = 32$ entradas possíveis.</span><span class="sxs-lookup"><span data-stu-id="6fb58-138">The `ReflectAboutMarked` operation is called only four times, but your Q# program was able to find the "01010" input amongst $2^{5} = 32$ possible inputs!</span></span>

## <a name="next-steps"></a><span data-ttu-id="6fb58-139">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="6fb58-139">Next steps</span></span>

<span data-ttu-id="6fb58-140">Se você gostou deste início rápido, confira alguns dos recursos abaixo para saber mais sobre como usar o Q# para escrever seus próprios aplicativos quânticos:</span><span class="sxs-lookup"><span data-stu-id="6fb58-140">If you enjoyed this quickstart, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="6fb58-141">Volte para o guia de Introdução ao QDK</span><span class="sxs-lookup"><span data-stu-id="6fb58-141">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="6fb58-142">Experimente uma [amostra](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search) mais geral do algoritmo de pesquisa de Grover</span><span class="sxs-lookup"><span data-stu-id="6fb58-142">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="6fb58-143">Saiba mais sobre a pesquisa de Grover com o Quantum Katas</span><span class="sxs-lookup"><span data-stu-id="6fb58-143">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="6fb58-144">Leia mais sobre a [Amplificação de amplitude](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), a técnica de computação quântica por trás do algoritmo de pesquisa de Grover</span><span class="sxs-lookup"><span data-stu-id="6fb58-144">Read more about [Amplitude amplification](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="6fb58-145">Conceitos da computação quântica</span><span class="sxs-lookup"><span data-stu-id="6fb58-145">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="6fb58-146">Amostras do Quantum development kit</span><span class="sxs-lookup"><span data-stu-id="6fb58-146">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
