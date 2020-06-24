---
title: Criar seu próprio classificador com o QDK
description: Conheça os conceitos básicos da criação de modelos de circuito para o classificador de circuito do Quantum.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/17/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.design
ms.openlocfilehash: b304b9d1a15f164f4dfe758aaed31b7b2369b18c
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274321"
---
# <a name="design-your-own-classifier"></a><span data-ttu-id="0ea00-103">Criar seu classificador</span><span class="sxs-lookup"><span data-stu-id="0ea00-103">Design your own classifier</span></span>

<span data-ttu-id="0ea00-104">Neste guia, você aprenderá os conceitos básicos por trás do design de modelos de circuito para o classificador centrado no circuito Quantum.</span><span class="sxs-lookup"><span data-stu-id="0ea00-104">In this guide you will learn the basic concepts behind the design of circuit models for the quantum circuit centric classifier.</span></span>

<span data-ttu-id="0ea00-105">Como no aprendizado profundo clássico, não há nenhuma regra geral para escolher uma arquitetura específica.</span><span class="sxs-lookup"><span data-stu-id="0ea00-105">As in classical deep learning, there is no general rule for choosing a specific architecture.</span></span> <span data-ttu-id="0ea00-106">Dependendo do problema, algumas arquiteturas terão um desempenho melhor do que outras.</span><span class="sxs-lookup"><span data-stu-id="0ea00-106">Depending on the problem some architectures will perform better than others.</span></span> <span data-ttu-id="0ea00-107">Mas, há alguns conceitos que podem ser úteis ao criar o circuito:</span><span class="sxs-lookup"><span data-stu-id="0ea00-107">But, there are some concepts that might be useful when designing the circuit:</span></span>

- <span data-ttu-id="0ea00-108">Um grande número de parâmetros implica um modelo mais flexível, que pode ser adequado para desenhar limites de classificação complicados, mas que também podem ser mais suscetíveis a sobreajuste.</span><span class="sxs-lookup"><span data-stu-id="0ea00-108">A large number of parameters implies a more flexible model, which may be suitable to draw complicated classification boundaries but which may also be more susceptible to overfitting.</span></span>

- <span data-ttu-id="0ea00-109">Entangling Gates entre qubits são essenciais para capturar as correlações entre os recursos do Quantum.</span><span class="sxs-lookup"><span data-stu-id="0ea00-109">Entangling gates between qubits are essential to capture the correlations between the quantum features.</span></span>

## <a name="how-to-build-a-classifier-with-q"></a><span data-ttu-id="0ea00-110">Como criar um classificador com Q\#</span><span class="sxs-lookup"><span data-stu-id="0ea00-110">How to build a classifier with Q\#</span></span>

<span data-ttu-id="0ea00-111">Para criar um classificador, vamos concatenar as rotações controladas pelo parametrizadas em nosso modelo de circuito.</span><span class="sxs-lookup"><span data-stu-id="0ea00-111">To build a classifier we are going to concatenate parametrized controlled rotations in our circuit model.</span></span> <span data-ttu-id="0ea00-112">Para fazer isso, podemos usar o tipo [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) definido na biblioteca de Machine Learning Quantum.</span><span class="sxs-lookup"><span data-stu-id="0ea00-112">To do it we can use the type [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) defined in the Quantum Machine Learning library.</span></span> <span data-ttu-id="0ea00-113">Esse tipo aceita quatro argumentos que determinam: o índice do qubit de destino, a matriz de índices do controle qubits, o eixo de rotação e o índice do parâmetro associado na matriz de parâmetros que definem o modelo.</span><span class="sxs-lookup"><span data-stu-id="0ea00-113">This type accepts four arguments that determine: the index of the target qubit, the array of indices of the control qubits, the axis of rotation, and index of the associated parameter in the array of parameters defining the model.</span></span>

<span data-ttu-id="0ea00-114">Vejamos um exemplo de classificador.</span><span class="sxs-lookup"><span data-stu-id="0ea00-114">Let's see an example of a classifier.</span></span> <span data-ttu-id="0ea00-115">No [exemplo de meia lua](https://github.com/microsoft/Quantum/tree/master/samples/machine-learning/half-moons), podemos encontrar o classificador a seguir definido no arquivo `Training.qs` .</span><span class="sxs-lookup"><span data-stu-id="0ea00-115">In the [half-moons sample](https://github.com/microsoft/Quantum/tree/master/samples/machine-learning/half-moons), we can find the following classifier defined in the file `Training.qs`.</span></span>

```qsharp
    function ClassifierStructure() : ControlledRotation[] {
        return [
            ControlledRotation((0, new Int[0]), PauliX, 4),
            ControlledRotation((0, new Int[0]), PauliZ, 5),
            ControlledRotation((1, new Int[0]), PauliX, 6),
            ControlledRotation((1, new Int[0]), PauliZ, 7),
            ControlledRotation((0, [1]), PauliX, 0),
            ControlledRotation((1, [0]), PauliX, 1),
            ControlledRotation((1, new Int[0]), PauliZ, 2),
            ControlledRotation((1, new Int[0]), PauliX, 3)
        ];
    }
 ```

<span data-ttu-id="0ea00-116">O que estamos definindo aqui é uma função que retorna uma matriz de `ControlledRotation` elementos, que junto com uma matriz de parâmetros e uma tendência definirão nosso [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel) .</span><span class="sxs-lookup"><span data-stu-id="0ea00-116">What we are defining here is a function that returns an array of `ControlledRotation` elements, that together with an array of parameters and a bias will define our [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel).</span></span> <span data-ttu-id="0ea00-117">Esse tipo é fundamental na biblioteca de Machine Learning Quantum e define o classificador.</span><span class="sxs-lookup"><span data-stu-id="0ea00-117">This type is fundamental in the Quantum Machine Learning library and defines the classifier.</span></span> <span data-ttu-id="0ea00-118">O circuito definido na função acima faz parte de um classificador no qual cada amostra do conjunto de um contém dois recursos.</span><span class="sxs-lookup"><span data-stu-id="0ea00-118">The circuit defined in the function above is part of a classifier in which each sample of the dataset contains two features.</span></span> <span data-ttu-id="0ea00-119">Portanto, precisamos apenas de dois qubits.</span><span class="sxs-lookup"><span data-stu-id="0ea00-119">Therefore we only need two qubits.</span></span> <span data-ttu-id="0ea00-120">A representação gráfica do circuito é:</span><span class="sxs-lookup"><span data-stu-id="0ea00-120">The graphical representation of the circuit is:</span></span>

 ![Exemplo de modelo de circuito](~/media/circuit_model_1.PNG)

## <a name="use-the-library-functions-to-write-layers-of-gates"></a><span data-ttu-id="0ea00-122">Usar as funções de biblioteca para gravar camadas de Gates</span><span class="sxs-lookup"><span data-stu-id="0ea00-122">Use the library functions to write layers of gates</span></span>

<span data-ttu-id="0ea00-123">Suponha que tenhamos um DataSet com 784 recursos por instância, por exemplo, imagens de 28 × 28 pixels, como o conjunto de MNIST.</span><span class="sxs-lookup"><span data-stu-id="0ea00-123">Suppose we have a dataset with 784 features per instance, e.g. images of 28×28 pixels like the MNIST dataset.</span></span> <span data-ttu-id="0ea00-124">Nesse caso, a largura do circuito se torna grande o suficiente para que a gravação manual de cada portão se torne uma tarefa possível, mas impraticável.</span><span class="sxs-lookup"><span data-stu-id="0ea00-124">In this case, the width of the circuit becomes large enough so that writing by hand each individual gate becomes a possible but impractical task.</span></span> <span data-ttu-id="0ea00-125">É por isso que a biblioteca de Machine Learning Quantum fornece um conjunto de ferramentas para gerar automaticamente camadas de rotações de parametrizadas.</span><span class="sxs-lookup"><span data-stu-id="0ea00-125">This is why the Quantum Machine Learning library provides a set of tools to automatically generate layers of parametrized rotations.</span></span> <span data-ttu-id="0ea00-126">Por exemplo, a função [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) retorna uma matriz de rotações de qubit simples não controladas ao longo de um determinado eixo, com uma rotação para cada qubit no registro, cada parametrizadas por um parâmetro de modelo diferente.</span><span class="sxs-lookup"><span data-stu-id="0ea00-126">For instance, the function [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) returns an array of uncontrolled single-qubit rotations along a given axis, with one rotation for each qubit in the register, each parametrized by a different model parameter.</span></span> <span data-ttu-id="0ea00-127">Por exemplo, `LocalRotationsLayer(4, X)` retorna o seguinte conjunto de Gates:</span><span class="sxs-lookup"><span data-stu-id="0ea00-127">For example, `LocalRotationsLayer(4, X)` returns the following set of gates:</span></span>

 ![Camada de rotações locais](~/media/local_rotations_layer.PNG)

<span data-ttu-id="0ea00-129">Recomendamos que você explore a [referência de API da biblioteca de Machine Learning Quantum](xref:microsoft.quantum.machinelearning) para descobrir todas as ferramentas disponíveis para simplificar o design do circuito.</span><span class="sxs-lookup"><span data-stu-id="0ea00-129">We recommend you explore the [API reference of the Quantum Machine Learning library](xref:microsoft.quantum.machinelearning) to discover all the tools available to streamline the circuit design.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0ea00-130">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="0ea00-130">Next steps</span></span>

 <span data-ttu-id="0ea00-131">Experimente estruturas diferentes nos exemplos fornecidos pelos exemplos.</span><span class="sxs-lookup"><span data-stu-id="0ea00-131">Try different structures in the examples provided by the samples.</span></span> <span data-ttu-id="0ea00-132">Você vê as alterações no desempenho do modelo?</span><span class="sxs-lookup"><span data-stu-id="0ea00-132">Do you see any changes in the performance of the model?</span></span> <span data-ttu-id="0ea00-133">No próximo tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load) você aprenderá a carregar conjuntos de valores para experimentar e explorar novas arquiteturas de classificadores.</span><span class="sxs-lookup"><span data-stu-id="0ea00-133">In the next tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load), you will learn how to load datasets to try and explore new architectures of classifiers.</span></span>
