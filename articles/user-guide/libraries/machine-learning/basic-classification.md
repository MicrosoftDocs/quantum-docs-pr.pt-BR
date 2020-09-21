---
title: Classificação básica com a biblioteca de Machine Learning Quantum
description: Saiba como executar um classificador sequencial Quantum escrito em Q# usando a biblioteca de Machine Learning Quantum do Microsoft QDK.
author: geduardo
ms.author: v-edsanc
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5dc4614b9992e2c6b9f8ff4b839c0929ec8cab7c
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833714"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a><span data-ttu-id="caf5c-103">Classificação básica: classificar dados com o QDK</span><span class="sxs-lookup"><span data-stu-id="caf5c-103">Basic classification: Classify data with the QDK</span></span>

<span data-ttu-id="caf5c-104">Neste guia de início rápido, você aprenderá a executar um classificador sequencial Quantum escrito em Q# usando a biblioteca de Machine Learning Quantum do QDK.</span><span class="sxs-lookup"><span data-stu-id="caf5c-104">In this Quickstart, you will learn how to run a quantum sequential classifier written in Q# using the Quantum Machine Learning library of the QDK.</span></span> 

<span data-ttu-id="caf5c-105">Neste guia, usaremos o conjunto de dados de meia lua, usando uma estrutura de classificador definida em Q# .</span><span class="sxs-lookup"><span data-stu-id="caf5c-105">In this guide we will use the half-moon dataset, using a classifier structure defined in Q#.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="caf5c-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="caf5c-106">Prerequisites</span></span>

- <span data-ttu-id="caf5c-107">O Microsoft [Quantum development kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="caf5c-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="caf5c-108">Crie um Q# projeto para um [programa de host Python](xref:microsoft.quantum.install.python) ou para um [programa de host C#](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="caf5c-108">Create a Q# project for either a [Python host program](xref:microsoft.quantum.install.python) or a [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="host-program"></a><span data-ttu-id="caf5c-109">Programa de host</span><span class="sxs-lookup"><span data-stu-id="caf5c-109">Host program</span></span>

<span data-ttu-id="caf5c-110">O programa de host consiste em três partes:</span><span class="sxs-lookup"><span data-stu-id="caf5c-110">Your host program consists of three parts:</span></span>

- <span data-ttu-id="caf5c-111">Carregue o conjunto de e escolha um conjunto de parâmetros iniciais para seu modelo.</span><span class="sxs-lookup"><span data-stu-id="caf5c-111">Load the dataset and choose a set of starting parameters for your model.</span></span>
- <span data-ttu-id="caf5c-112">Execute o treinamento para determinar os parâmetros e a diferença do modelo.</span><span class="sxs-lookup"><span data-stu-id="caf5c-112">Run training to determine the parameters and bias of the model.</span></span>
- <span data-ttu-id="caf5c-113">Validar o modelo para determinar sua exatidão</span><span class="sxs-lookup"><span data-stu-id="caf5c-113">Validate the model to determine its accuracy</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="caf5c-114">Python com Visual Studio Code ou a linha de comando</span><span class="sxs-lookup"><span data-stu-id="caf5c-114">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="caf5c-115">Para executar você é o Q# classificador do Python, salve o código a seguir como `host.py` .</span><span class="sxs-lookup"><span data-stu-id="caf5c-115">To run your the Q# classifier from Python, save the following code as `host.py`.</span></span> <span data-ttu-id="caf5c-116">Lembre-se de que você também precisa do Q# arquivo `Training.qs` explicado posteriormente neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="caf5c-116">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    <span data-ttu-id="caf5c-117">Em seguida, execute o programa host do Python na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="caf5c-117">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="caf5c-118">C# com Visual Studio Code ou a linha de comando</span><span class="sxs-lookup"><span data-stu-id="caf5c-118">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="caf5c-119">Para executar você é o Q# classificador do C#, salve o código a seguir como `Host.cs` .</span><span class="sxs-lookup"><span data-stu-id="caf5c-119">To run your the Q# classifier from C#, save the following code as `Host.cs`.</span></span> <span data-ttu-id="caf5c-120">Lembre-se de que você também precisa do Q# arquivo `Training.qs` explicado posteriormente neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="caf5c-120">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="caf5c-121">Em seguida, execute o programa host do C# na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="caf5c-121">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[<span data-ttu-id="caf5c-122">C# com Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="caf5c-122">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="caf5c-123">Para executar o novo Q# programa do C# no Visual Studio, modifique `Host.cs` para incluir o código C# a seguir.</span><span class="sxs-lookup"><span data-stu-id="caf5c-123">To run your new Q# program from C# in Visual Studio, modify `Host.cs` to include the following C# code.</span></span> <span data-ttu-id="caf5c-124">Lembre-se de que você também precisa do Q# arquivo `Training.qs` explicado posteriormente neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="caf5c-124">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="caf5c-125">Pressione F5 e o programa começará a ser executado.</span><span class="sxs-lookup"><span data-stu-id="caf5c-125">Press F5, and the program will start to run.</span></span> <span data-ttu-id="caf5c-126">Uma nova janela exibirá os seguintes resultados:</span><span class="sxs-lookup"><span data-stu-id="caf5c-126">A new window will display the following results:</span></span> 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a><span data-ttu-id="caf5c-127">\#Código do classificador Q</span><span class="sxs-lookup"><span data-stu-id="caf5c-127">Q\# classifier code</span></span>

<span data-ttu-id="caf5c-128">Agora, vejamos como as operações invocadas pelo programa de host estão definidas em Q# .</span><span class="sxs-lookup"><span data-stu-id="caf5c-128">Now let's see how the operations invoked by the host program are defined in Q#.</span></span>
<span data-ttu-id="caf5c-129">Salvamos o código a seguir em um arquivo chamado `Training.qs` .</span><span class="sxs-lookup"><span data-stu-id="caf5c-129">We save the following code in a file named `Training.qs`.</span></span>

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

<span data-ttu-id="caf5c-130">As funções e operações mais importantes definidas no código acima são:</span><span class="sxs-lookup"><span data-stu-id="caf5c-130">The most important functions and operations defined in the code above are:</span></span>

- <span data-ttu-id="caf5c-131">`ClassifierStructure() : ControlledRotation[]` : nessa função, definimos a estrutura do nosso modelo de circuito adicionando as camadas das Gates controladas que consideramos.</span><span class="sxs-lookup"><span data-stu-id="caf5c-131">`ClassifierStructure() : ControlledRotation[]` : in this function we set the structure of our circuit model by adding the layers of the controlled gates we consider.</span></span> <span data-ttu-id="caf5c-132">Esta etapa é análoga à declaração de camadas de neurônios em um modelo de aprendizado profundo sequencial.</span><span class="sxs-lookup"><span data-stu-id="caf5c-132">This step is analogous to the declaration of layers of neurons in a sequential deep learning model.</span></span>
- <span data-ttu-id="caf5c-133">`TrainHalfMoonModel() : (Double[], Double)` : essa operação é a parte principal do código e define o treinamento.</span><span class="sxs-lookup"><span data-stu-id="caf5c-133">`TrainHalfMoonModel() : (Double[], Double)` : this operation is the core part of the code and defines the training.</span></span> <span data-ttu-id="caf5c-134">Aqui, carregamos os exemplos do conjunto de conjuntos incluído na biblioteca, definimos os parâmetros do Hyper e os parâmetros iniciais para o treinamento e iniciamos o treinamento chamando a operação `TrainSequentialClassifier` incluída na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="caf5c-134">Here we load the samples from the dataset included in the library, we set the hyper parameters and the initial parameters for the training and we start the training by calling the operation `TrainSequentialClassifier` included in the library.</span></span> <span data-ttu-id="caf5c-135">Ele gera os parâmetros e a tendência que determinam o classificador.</span><span class="sxs-lookup"><span data-stu-id="caf5c-135">It outputs the parameters and the bias that determine the classifier.</span></span>
- <span data-ttu-id="caf5c-136">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : essa operação define o processo de validação para avaliar o modelo.</span><span class="sxs-lookup"><span data-stu-id="caf5c-136">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : this operation defines the validation process to evaluate the model.</span></span> <span data-ttu-id="caf5c-137">Aqui, carregamos os exemplos para validação, o número de medições por amostra e a tolerância.</span><span class="sxs-lookup"><span data-stu-id="caf5c-137">Here we load the samples for validation, the number of measurements per sample and the tolerance.</span></span> <span data-ttu-id="caf5c-138">Ele gera o número de classificações incorretas no lote escolhido de amostras para validação.</span><span class="sxs-lookup"><span data-stu-id="caf5c-138">It outputs the number of misclassifications on the chosen batch of samples for validation.</span></span>

## <a name="next-steps"></a><span data-ttu-id="caf5c-139">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="caf5c-139">Next steps</span></span>

<span data-ttu-id="caf5c-140">Primeiro, você pode brincar com o código e tentar alterar alguns parâmetros para ver como ele afeta o treinamento.</span><span class="sxs-lookup"><span data-stu-id="caf5c-140">First, you can play with the code and try to change some parameters to see how it affects the training.</span></span> <span data-ttu-id="caf5c-141">Em seguida, no próximo tutorial, [crie seu próprio classificador](xref:microsoft.quantum.libraries.machine-learning.design), você aprenderá a definir a estrutura do classificador.</span><span class="sxs-lookup"><span data-stu-id="caf5c-141">Then, in the next tutorial, [Design your own classifier](xref:microsoft.quantum.libraries.machine-learning.design),  you will learn how to define the structure of the classifier.</span></span>
