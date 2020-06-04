---
title: Carregando dados clássicos
description: Saiba como carregar seu próprio conjunto de informações para treinar um modelo de classificação com o Microsoft Quantum Development Kit (QDK).
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.load
ms.openlocfilehash: efa4a65a489446cbef48507d0b02a932da74c71c
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327655"
---
# <a name="load-and-classify-your-own-datasets"></a><span data-ttu-id="c1607-103">Carregar e classificar seus próprios conjuntos de valores</span><span class="sxs-lookup"><span data-stu-id="c1607-103">Load and classify your own datasets</span></span>

<span data-ttu-id="c1607-104">Neste breve tutorial, vamos aprender como carregar seu próprio conjunto de informações para treinar um modelo classificador com o kit de desenvolvimento Quantum (QDK).</span><span class="sxs-lookup"><span data-stu-id="c1607-104">In this short tutorial, we are going to learn how to load your own dataset to train a classifier model with the Quantum Development Kit (QDK).</span></span>

<span data-ttu-id="c1607-105">É altamente recomendável o uso de um formato de serialização padronizado, como [arquivos JSON](https://en.wikipedia.org/wiki/JSON) , para armazenar seus dados.</span><span class="sxs-lookup"><span data-stu-id="c1607-105">We highly recommend the use of a standardized serialization format such as [JSON files](https://en.wikipedia.org/wiki/JSON) to store your data.</span></span>
<span data-ttu-id="c1607-106">Esses formatos oferecem alta compatibilidade com estruturas diferentes, como Python e o ecossistema .NET.</span><span class="sxs-lookup"><span data-stu-id="c1607-106">Such formats offer high compatibility with different frameworks like Python and the .NET ecosystem.</span></span>
<span data-ttu-id="c1607-107">Em particular, é recomendável usar nosso modelo para carregar os dados, para que você possa copiar e colar o código diretamente dos exemplos.</span><span class="sxs-lookup"><span data-stu-id="c1607-107">In particular, we recommend using our template for loading the data, so that you can copy-paste the code directly from the samples.</span></span>

## <a name="template-for-loading-your-datasets"></a><span data-ttu-id="c1607-108">Modelo para carregar seus conjuntos de valores</span><span class="sxs-lookup"><span data-stu-id="c1607-108">Template for loading your datasets</span></span>

<span data-ttu-id="c1607-109">Suponha que tenhamos um conjunto de recursos de treinamento $ (x, y) $ de Size $N = $2, em que cada instância $x _i $ of $x $ tem três recursos: $x _ {I1} $, $x _ {I2} $ e $x _ {i3} $.</span><span class="sxs-lookup"><span data-stu-id="c1607-109">Suppose we have a training dataset $(x, y)$ of size $N=2$ where each instance $x_i$ of $x$ has three features: $x_{i1}$, $x_{i2}$ and $x_{i3}$.</span></span>
<span data-ttu-id="c1607-110">O conjunto de dados de validação tem a mesma estrutura.</span><span class="sxs-lookup"><span data-stu-id="c1607-110">The validation dataset has the same structure.</span></span>
<span data-ttu-id="c1607-111">Esses conjuntos podem ser representados por um `data.json` arquivo semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="c1607-111">These datsets can be represented by a `data.json` file similar to the following:</span></span>

```json
{
    "TrainingData": {
        "Features": [
            [
                x_11,
                x_12,
                x_13
            ],
            [
                x_21,
                x_22,
                x_23
            ]
        ],
        "Labels": [
            y_1,
            y_2
        ]
    },
    "ValidationData": {
        "Features": [
            [
                xv_11,
                xv_12,
                xv_13
            ],
            [
                xv_11,
                xv_12,
                xv_13
            ]
        ],
        "Labels": [
            yv_1,
            yv_2
        ]
    }
}
```

### <a name="example-using-the-template"></a><span data-ttu-id="c1607-112">Exemplo usando o modelo</span><span class="sxs-lookup"><span data-stu-id="c1607-112">Example using the template</span></span>

<span data-ttu-id="c1607-113">Suponha que tenhamos um pequeno conjunto de pequenos com as alturas e os pesos de diferentes gatos e cachorros.</span><span class="sxs-lookup"><span data-stu-id="c1607-113">Suppose we have a small dataset with the heights and weights of different cats and dogs.</span></span> <span data-ttu-id="c1607-114">Esse conjunto de espaço de os é muito pequeno para treinar um modelo, mas será suficiente para mostrar o processo de carregamento de um conjunto de um DataSet.</span><span class="sxs-lookup"><span data-stu-id="c1607-114">This dataset is very small to train a model but will be enough to show the process of loading a dataset.</span></span>

| <span data-ttu-id="c1607-115">Altura (m)</span><span class="sxs-lookup"><span data-stu-id="c1607-115">Height (m)</span></span> | <span data-ttu-id="c1607-116">Peso (kg)</span><span class="sxs-lookup"><span data-stu-id="c1607-116">Weight (kg)</span></span> | <span data-ttu-id="c1607-117">Animal</span><span class="sxs-lookup"><span data-stu-id="c1607-117">Animal</span></span> |
|-----------|------------|--------|
| <span data-ttu-id="c1607-118">0,54</span><span class="sxs-lookup"><span data-stu-id="c1607-118">0.54</span></span>      | <span data-ttu-id="c1607-119">30</span><span class="sxs-lookup"><span data-stu-id="c1607-119">30</span></span>         | <span data-ttu-id="c1607-120">Auto</span><span class="sxs-lookup"><span data-stu-id="c1607-120">Dog</span></span>    |
| <span data-ttu-id="c1607-121">0,30</span><span class="sxs-lookup"><span data-stu-id="c1607-121">0.30</span></span>      | <span data-ttu-id="c1607-122">8</span><span class="sxs-lookup"><span data-stu-id="c1607-122">8</span></span>          | <span data-ttu-id="c1607-123">Cat</span><span class="sxs-lookup"><span data-stu-id="c1607-123">Cat</span></span>    |
| <span data-ttu-id="c1607-124">0.91</span><span class="sxs-lookup"><span data-stu-id="c1607-124">0.91</span></span>      | <span data-ttu-id="c1607-125">44</span><span class="sxs-lookup"><span data-stu-id="c1607-125">44</span></span>         | <span data-ttu-id="c1607-126">Auto</span><span class="sxs-lookup"><span data-stu-id="c1607-126">Dog</span></span>    |
| <span data-ttu-id="c1607-127">0.86</span><span class="sxs-lookup"><span data-stu-id="c1607-127">0.86</span></span>      | <span data-ttu-id="c1607-128">31</span><span class="sxs-lookup"><span data-stu-id="c1607-128">31</span></span>          | <span data-ttu-id="c1607-129">Auto</span><span class="sxs-lookup"><span data-stu-id="c1607-129">Dog</span></span>    |
| <span data-ttu-id="c1607-130">0,32</span><span class="sxs-lookup"><span data-stu-id="c1607-130">0.32</span></span>      | <span data-ttu-id="c1607-131">5</span><span class="sxs-lookup"><span data-stu-id="c1607-131">5</span></span>         | <span data-ttu-id="c1607-132">Cat</span><span class="sxs-lookup"><span data-stu-id="c1607-132">Cat</span></span>    |
| <span data-ttu-id="c1607-133">0.25</span><span class="sxs-lookup"><span data-stu-id="c1607-133">0.25</span></span>      | <span data-ttu-id="c1607-134">4</span><span class="sxs-lookup"><span data-stu-id="c1607-134">4</span></span>          | <span data-ttu-id="c1607-135">Cat</span><span class="sxs-lookup"><span data-stu-id="c1607-135">Cat</span></span>    |

<span data-ttu-id="c1607-136">O processo é:</span><span class="sxs-lookup"><span data-stu-id="c1607-136">The process is:</span></span>

- <span data-ttu-id="c1607-137">Primeiro, precisamos separar o DataSet em treinamento e validação.</span><span class="sxs-lookup"><span data-stu-id="c1607-137">First we need to separate the dataset into training and validation.</span></span> <span data-ttu-id="c1607-138">Nesse caso, podemos apenas usar os três primeiros exemplos para treinamento e o restante dos exemplos para validação.</span><span class="sxs-lookup"><span data-stu-id="c1607-138">In this case we can just take the first three samples for training and the rest of samples for validation.</span></span> <span data-ttu-id="c1607-139">Em geral, é uma boa prática para fazer amostras aleatoriamente do conjunto de dados de treinamento e validação para evitar dipolaridades indesejadas no dado de treinamento.</span><span class="sxs-lookup"><span data-stu-id="c1607-139">In general it is a good practice to sample randomly the training and validation dataset to avoid unwanted biases in the training data.</span></span>
- <span data-ttu-id="c1607-140">Em segundo lugar, precisamos atribuir um rótulo numérico a cada classe.</span><span class="sxs-lookup"><span data-stu-id="c1607-140">Secondly, we need to assign a numeric label to each class.</span></span> <span data-ttu-id="c1607-141">Observe que, por enquanto, a biblioteca QML admite apenas problemas de classificação binária.</span><span class="sxs-lookup"><span data-stu-id="c1607-141">Note that, for the moment, the QML library only admits binary classification problems.</span></span> <span data-ttu-id="c1607-142">Portanto, atribuíremos o rótulo 0 à classe `Dog` e o número 1 à classe `Cat` .</span><span class="sxs-lookup"><span data-stu-id="c1607-142">So we will assign the label 0 to the class `Dog` and the number 1 to the class `Cat`.</span></span>
- <span data-ttu-id="c1607-143">Por fim, preenchemos o modelo usando os dados do nosso conjunto.</span><span class="sxs-lookup"><span data-stu-id="c1607-143">Finally, we fill the template using the data from our dataset.</span></span> <span data-ttu-id="c1607-144">Observe que, para conjuntos de grandes DataSets, você deve criar um pequeno script para gerar automaticamente o modelo de seu conjunto de informações específico.</span><span class="sxs-lookup"><span data-stu-id="c1607-144">Note that for big datasets you should build a small script to automatically generate the template from your specific dataset.</span></span> <span data-ttu-id="c1607-145">Esse script dependerá do formato original do conjunto de seus conjuntos de seus.</span><span class="sxs-lookup"><span data-stu-id="c1607-145">This script will depend on the original format of your dataset.</span></span>

<span data-ttu-id="c1607-146">Para nosso conjunto de nossos, o `data.json` arquivo é:</span><span class="sxs-lookup"><span data-stu-id="c1607-146">For our dataset the `data.json` file is:</span></span>

```json
{
    "TrainingData": {
        "Features": [
            [
                0.54,
                30
            ],
            [
                0.30,
                8
            ],
            [
                0.91,
                44
            ]
        ],
        "Labels": [
            0,
            1,
            0
        ]
    },
    "ValidationData": {
        "Features": [
            [
                0.86,
                31
            ],
            [
                0.32,
                5
            ]
            [
                0.25,
                4
            ]
        ],
        "Labels": [
            0,
            1,
            1
        ]
    }
}

```

## <a name="loading-the-data"></a><span data-ttu-id="c1607-147">Carregando os dados</span><span class="sxs-lookup"><span data-stu-id="c1607-147">Loading the data</span></span>

<span data-ttu-id="c1607-148">Depois que os dados forem serializados como um arquivo JSON, você poderá carregá-los usando as bibliotecas JSON fornecidas com o idioma do host escolhido.</span><span class="sxs-lookup"><span data-stu-id="c1607-148">Once you have your data serialized as a JSON file, you can load it in using JSON libraries provided with your host language of choice.</span></span>

### <a name="python"></a>[<span data-ttu-id="c1607-149">Python</span><span class="sxs-lookup"><span data-stu-id="c1607-149">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="c1607-150">O Python fornece o [ `json` pacote interno](https://docs.python.org/3.7/library/json.html) para trabalhar com dados serializados em JSON:</span><span class="sxs-lookup"><span data-stu-id="c1607-150">Python provides the [built-in `json` package](https://docs.python.org/3.7/library/json.html) for working with JSON-serialized data:</span></span>

:::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="4-5,20-22":::

### <a name="c"></a>[<span data-ttu-id="c1607-151">C#</span><span class="sxs-lookup"><span data-stu-id="c1607-151">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="c1607-152">A plataforma .NET Core fornece o [ `System.Text.Json` pacote](https://www.nuget.org/packages/System.Text.Json) para trabalhar com dados serializados em JSON:</span><span class="sxs-lookup"><span data-stu-id="c1607-152">The .NET Core platform provides the [`System.Text.Json` package](https://www.nuget.org/packages/System.Text.Json) for working with JSON-serialized data:</span></span>

:::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="10,64-82":::

***

## <a name="next-steps"></a><span data-ttu-id="c1607-153">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="c1607-153">Next steps</span></span>

<span data-ttu-id="c1607-154">Agora você está pronto para começar a executar seus próprios experimentos com seus próprios conjuntos de valores.</span><span class="sxs-lookup"><span data-stu-id="c1607-154">Now you are ready to start running your own experiments with your own datasets.</span></span> <span data-ttu-id="c1607-155">Experimente classificadores e conjuntos de resultados diferentes e contribua para a Comunidade que está compartilhando seu resultado!</span><span class="sxs-lookup"><span data-stu-id="c1607-155">Try different classifiers and dataset and contribute to the community sharing your results!</span></span>
