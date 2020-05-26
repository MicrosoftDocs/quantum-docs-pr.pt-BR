---
title: Executar o algoritmo de pesquisa de Grover em Q# – Quantum development kit
description: Crie um projeto Q# que demonstra o algoritmo de Grover, um dos algoritmos quânticos canônicos.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 9562e1937a2cac49d682cc0524d8fb29e276d95c
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426802"
---
# <a name="tutorial-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="a69a4-103">Tutorial: Implementar o algoritmo de pesquisa de Grover em Q\#</span><span class="sxs-lookup"><span data-stu-id="a69a4-103">Tutorial: Implement Grover's search algorithm in Q\#</span></span>

<span data-ttu-id="a69a4-104">Neste tutorial, saiba como criar e executar a pesquisa de Grover para acelerar a pesquisa de dados não estruturados.</span><span class="sxs-lookup"><span data-stu-id="a69a4-104">In this tutorial, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="a69a4-105">A pesquisa de Grover é um dos algoritmos de computação quântica mais populares e essa implementação do Q# relativamente pequena dá uma noção das vantagens da programação de soluções quânticas com uma linguagem de programação quântica Q# de alto nível para expressar algoritmos quânticos.</span><span class="sxs-lookup"><span data-stu-id="a69a4-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="a69a4-106">No final do guia, você verá que a saída de simulação demonstra com êxito a localização de uma cadeia de caracteres específica entre uma lista de entradas não ordenadas em uma fração do tempo que levaria para pesquisar a lista inteira em um computador clássico.</span><span class="sxs-lookup"><span data-stu-id="a69a4-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of unordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="a69a4-107">O algoritmo de Grover pesquisa itens específicos em uma lista de dados não estruturados.</span><span class="sxs-lookup"><span data-stu-id="a69a4-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="a69a4-108">Por exemplo, ele pode responder à pergunta: Esta carta retirada de um baralho é um ás de copas?</span><span class="sxs-lookup"><span data-stu-id="a69a4-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="a69a4-109">A rotulagem do item específico é chamada _entrada marcada_.</span><span class="sxs-lookup"><span data-stu-id="a69a4-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="a69a4-110">Usando o algoritmo de pesquisa de Grover, é garantido que um computador quântico execute essa pesquisa em menos etapas do que o número de itens na lista que você está pesquisando – algo que nenhum algoritmo clássico pode fazer.</span><span class="sxs-lookup"><span data-stu-id="a69a4-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="a69a4-111">A maior velocidade no caso de um baralho é insignificante; no entanto, em listas que contêm milhões ou bilhões de itens, ela se torna significativa.</span><span class="sxs-lookup"><span data-stu-id="a69a4-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="a69a4-112">Você pode criar o algoritmo de pesquisa de Grover com apenas algumas linhas de código.</span><span class="sxs-lookup"><span data-stu-id="a69a4-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a69a4-113">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a69a4-113">Prerequisites</span></span>

- <span data-ttu-id="a69a4-114">O Microsoft [Quantum development kit][install].</span><span class="sxs-lookup"><span data-stu-id="a69a4-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="a69a4-115">O que o algoritmo de pesquisa de Grover faz?</span><span class="sxs-lookup"><span data-stu-id="a69a4-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="a69a4-116">O algoritmo de Grover pergunta se um item de uma lista é aquele que estamos procurando.</span><span class="sxs-lookup"><span data-stu-id="a69a4-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="a69a4-117">Ele faz isso construindo uma superposição quântica dos índices da lista com cada coeficiente, ou amplitude de probabilidade, representando a probabilidade desse índice específico ser aquele que você está procurando.</span><span class="sxs-lookup"><span data-stu-id="a69a4-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="a69a4-118">No centro do algoritmo há duas etapas que aumentam de maneira incremental o coeficiente do índice que estamos procurando, até a amplitude da probabilidade desse coeficiente se aproximar de um.</span><span class="sxs-lookup"><span data-stu-id="a69a4-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="a69a4-119">O número de aumentos incrementais é menor que o número de itens na lista.</span><span class="sxs-lookup"><span data-stu-id="a69a4-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="a69a4-120">É por isso que o algoritmo de pesquisa de Grover executa a pesquisa em menos etapas do que qualquer algoritmo clássico.</span><span class="sxs-lookup"><span data-stu-id="a69a4-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Diagrama funcional do algoritmo de pesquisa de Grover](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="a69a4-122">Escreva o código</span><span class="sxs-lookup"><span data-stu-id="a69a4-122">Write the code</span></span>

1. <span data-ttu-id="a69a4-123">Usando o Quantum development kit, [crie um projeto Q#](xref:microsoft.quantum.howto.createproject) chamado `Grover` no ambiente de desenvolvimento de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="a69a4-123">Using the Quantum Development Kit, [create a new Q# project](xref:microsoft.quantum.howto.createproject) called `Grover`, in your development environment of choice.</span></span>

1. <span data-ttu-id="a69a4-124">Adicione o seguinte código ao arquivo `Program.qs` no novo projeto:</span><span class="sxs-lookup"><span data-stu-id="a69a4-124">Add the following code to the `Program.qs` file in your new project:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. <span data-ttu-id="a69a4-125">Para definir a lista que estamos pesquisando, crie um arquivo `Reflections.qs` e cole o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="a69a4-125">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    <span data-ttu-id="a69a4-126">A operação `ReflectAboutMarked` define a entrada marcada que você está pesquisando: a cadeia de caracteres que alterna zeros e uns.</span><span class="sxs-lookup"><span data-stu-id="a69a4-126">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="a69a4-127">Essa amostra embute a entrada marcada em código e pode ser estendida para pesquisar diferentes entradas ou generalizada para qualquer entrada.</span><span class="sxs-lookup"><span data-stu-id="a69a4-127">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="a69a4-128">Em seguida, execute o novo programa Q# para encontrar o item marcado por `ReflectAboutMarked`.</span><span class="sxs-lookup"><span data-stu-id="a69a4-128">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a><span data-ttu-id="a69a4-129">Aplicativos de linha de comando Q# com o Visual Studio ou com o Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a69a4-129">Q# command line applications with Visual Studio or Visual Studio Code</span></span>

<span data-ttu-id="a69a4-130">O executável executará a operação ou a função marcada com o atributo `@EntryPoint()` em um simulador ou em um avaliador de recurso, dependendo da configuração do projeto e das opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a69a4-130">The executable will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

<span data-ttu-id="a69a4-131">No Visual Studio, basta pressionar Ctrl + F5 para executar o script.</span><span class="sxs-lookup"><span data-stu-id="a69a4-131">In Visual Studio, simply press Ctrl + F5 to execute the script.</span></span>

<span data-ttu-id="a69a4-132">No VS Code, compile o `Program.qs` pela primeira vez digitando o seguinte no terminal:</span><span class="sxs-lookup"><span data-stu-id="a69a4-132">In VS Code, build the `Program.qs` the first time by typing the below in the terminal:</span></span>

```Command line
dotnet build
```

<span data-ttu-id="a69a4-133">Para as próximas execuções, não é necessário compilá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="a69a4-133">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="a69a4-134">Para executá-lo, digite o seguinte comando e pressione Enter:</span><span class="sxs-lookup"><span data-stu-id="a69a4-134">To run it, type the following command and press enter:</span></span>

```Command line
dotnet run --no-build
```

<span data-ttu-id="a69a4-135">Você deveria ver a seguinte mensagem exibida no terminal:</span><span class="sxs-lookup"><span data-stu-id="a69a4-135">You should see the following message displayed in the terminal:</span></span>

```
operations.qs:
This operation applies Grover's algorithm to search all possible inputs to an operation to find a particular marked state.
Usage:
operations.qs [options] [command]

--n-qubits <n-qubits> (REQUIRED)
-s, --simulator <simulator>         The name of the simulator to use.
--version                           Show version information
-?, -h, --help                      Show help and usage information
Commands:
```

<span data-ttu-id="a69a4-136">Isso ocorre porque você não especificou o número de qubits que desejava usar. Portanto, o terminal informa os comandos disponíveis para o executável.</span><span class="sxs-lookup"><span data-stu-id="a69a4-136">This is because you didn't specify the number of qubits you wanted to use, so the terminal tells you the commands available for the executable.</span></span> <span data-ttu-id="a69a4-137">Se desejamos usar cinco qubits, devemos digitar:</span><span class="sxs-lookup"><span data-stu-id="a69a4-137">If we want to use 5 qubits we should type:</span></span>

```Command line
dotnet run --n-qubits 5
```

<span data-ttu-id="a69a4-138">Ao pressionar Enter, você deveria ver a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="a69a4-138">Pressing enter you should see the following output:</span></span>

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a><span data-ttu-id="a69a4-139">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="a69a4-139">Next steps</span></span>

<span data-ttu-id="a69a4-140">Se você gostou deste tutorial, confira alguns dos recursos abaixo para saber mais sobre como usar o Q# para escrever aplicativos quânticos próprios:</span><span class="sxs-lookup"><span data-stu-id="a69a4-140">If you enjoyed this tutorial, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="a69a4-141">Volte para o guia de Introdução ao QDK</span><span class="sxs-lookup"><span data-stu-id="a69a4-141">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="a69a4-142">Experimente uma [amostra](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search) mais geral do algoritmo de pesquisa de Grover</span><span class="sxs-lookup"><span data-stu-id="a69a4-142">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="a69a4-143">Saiba mais sobre a pesquisa de Grover com o Quantum Katas</span><span class="sxs-lookup"><span data-stu-id="a69a4-143">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="a69a4-144">Leia mais sobre a [Amplificação de amplitude][amplitude-amplification], a técnica de computação quântica por trás do algoritmo de pesquisa de Grover</span><span class="sxs-lookup"><span data-stu-id="a69a4-144">Read more about [Amplitude amplification][amplitude-amplification], the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="a69a4-145">Conceitos da computação quântica</span><span class="sxs-lookup"><span data-stu-id="a69a4-145">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="a69a4-146">Amostras do Quantum development kit</span><span class="sxs-lookup"><span data-stu-id="a69a4-146">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification
