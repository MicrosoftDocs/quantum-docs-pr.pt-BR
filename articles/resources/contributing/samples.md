---
title: Colaborando com exemplos no Microsoft QDK
description: Saiba como contribuir com código de exemplo para a Microsoft Quantum Development Kit (QDK).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
ms.openlocfilehash: 3bd0de04a448c74eea6c3e8e3a15dcbb19f9d705
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274237"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a><span data-ttu-id="469fe-103">Colaborando com exemplos do kit de desenvolvimento Quantum</span><span class="sxs-lookup"><span data-stu-id="469fe-103">Contributing Samples to the Quantum Development Kit</span></span>

<span data-ttu-id="469fe-104">Se você estiver interessado em contribuir com código para o [repositório de exemplos](https://github.com/Microsoft/Quantum), obrigado por tornar a comunidade de desenvolvimento do Quantum um lugar melhor!</span><span class="sxs-lookup"><span data-stu-id="469fe-104">If you're interested in contributing code to the [samples repository](https://github.com/Microsoft/Quantum), thank you for making the quantum development community a better place!</span></span>

## <a name="the-quantum-development-kit-samples-repository"></a><span data-ttu-id="469fe-105">O repositório de exemplos do kit de desenvolvimento Quantum</span><span class="sxs-lookup"><span data-stu-id="469fe-105">The Quantum Development Kit Samples Repository</span></span>

<span data-ttu-id="469fe-106">Para ajudá-lo a preparar sua contribuição para ajudar o máximo possível, é útil dar uma olhada rápida em como o repositório de exemplos é apresentado:</span><span class="sxs-lookup"><span data-stu-id="469fe-106">To help you prepare your contribution to help out as much as possible, it's helpful to take a quick look at how the samples repository is laid out:</span></span>

```plaintext
microsoft/Quantum
📁 samples/
  📁 algorithms/
    📁 chsh-game/
      📝 CHSHGame.csproj
      📝 Game.qs
      📝 Host.cs
      📝 host.py
      📝 README.md
     ⋮
  📁 arithmetic/
  📁 characterization/
  📁 chemistry/
   ⋮
```

<span data-ttu-id="469fe-107">Ou seja, os exemplos no [repositório Microsoft/Quantum](https://github.com/microsoft/Quantum) são divididos por área de assunto em pastas diferentes, como `algorithms/` , `arithmetic/` ou `characterization/` .</span><span class="sxs-lookup"><span data-stu-id="469fe-107">That is, the samples in the [microsoft/Quantum repository](https://github.com/microsoft/Quantum) are broken down by subject area into different folders such as `algorithms/`, `arithmetic/`, or `characterization/`.</span></span>
<span data-ttu-id="469fe-108">Dentro da pasta de cada área de assunto, cada amostra consiste em uma única pasta que coleta tudo o que um usuário precisará para explorar e usar esse exemplo.</span><span class="sxs-lookup"><span data-stu-id="469fe-108">Within the folder for each subject area, each sample consists of a single folder that collects everything a user will need to explore and make use of that sample.</span></span>

## <a name="how-samples-are-structured"></a><span data-ttu-id="469fe-109">Como os exemplos são estruturados</span><span class="sxs-lookup"><span data-stu-id="469fe-109">How Samples are Structured</span></span>

<span data-ttu-id="469fe-110">Examinando os arquivos que compõem cada pasta, vamos nos aprofundar no [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) exemplo.</span><span class="sxs-lookup"><span data-stu-id="469fe-110">Looking at the files that make up each folder, let's dive into the [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) sample.</span></span>

| <span data-ttu-id="469fe-111">Arquivo</span><span class="sxs-lookup"><span data-stu-id="469fe-111">File</span></span>              | <span data-ttu-id="469fe-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="469fe-112">Description</span></span>                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | <span data-ttu-id="469fe-113">Projeto Q # usado para criar o exemplo com o SDK do .NET Core</span><span class="sxs-lookup"><span data-stu-id="469fe-113">Q# project used to build the sample with the .NET Core SDK</span></span> |
| `Game.qs`         | <span data-ttu-id="469fe-114">Q # operações e funções para o exemplo</span><span class="sxs-lookup"><span data-stu-id="469fe-114">Q# operations and functions for the sample</span></span>                 |
| `Host.cs`         | <span data-ttu-id="469fe-115">Programa de host C# usado para executar o exemplo</span><span class="sxs-lookup"><span data-stu-id="469fe-115">C# host program used to run the sample</span></span>                     |
| `host.py`         | <span data-ttu-id="469fe-116">Programa de host Python usado para executar o exemplo</span><span class="sxs-lookup"><span data-stu-id="469fe-116">Python host program used to run the sample</span></span>                 |
| `README.md`       | <span data-ttu-id="469fe-117">Documentação sobre o que o exemplo faz e como usá-lo</span><span class="sxs-lookup"><span data-stu-id="469fe-117">Documentation on what the sample does and how to use it</span></span>    |

<span data-ttu-id="469fe-118">Nem todos os exemplos terão exatamente o mesmo conjunto de arquivos (por exemplo: alguns exemplos podem ser somente em C#, outros podem não ter um host Python ou alguns exemplos podem exigir que arquivos de dados auxiliar funcionem).</span><span class="sxs-lookup"><span data-stu-id="469fe-118">Not all samples will have the exact same set of files (e.g.: some samples may be C#-only, others may not have a Python host, or some samples may require auxillary data files to work).</span></span>

## <a name="anatomy-of-a-helpful-readme-file"></a><span data-ttu-id="469fe-119">Anatomia de um arquivo LEIAme útil</span><span class="sxs-lookup"><span data-stu-id="469fe-119">Anatomy of a Helpful README File</span></span>

<span data-ttu-id="469fe-120">No entanto, um arquivo especialmente importante é o `README.md` arquivo, pois é isso que os usuários precisam para começar com seu exemplo!</span><span class="sxs-lookup"><span data-stu-id="469fe-120">One especially important file, though, is the `README.md` file, as that's what users need to get started with your sample!</span></span>

<span data-ttu-id="469fe-121">Cada um `README.md` deve começar com alguns metadados que ajudam a docs.Microsoft.com/samples a encontrar sua contribuição.</span><span class="sxs-lookup"><span data-stu-id="469fe-121">Each `README.md` should start with some metadata that helps docs.microsoft.com/samples find your contribution.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="469fe-122">Veja como o exemplo chsh-Game é renderizado</span><span class="sxs-lookup"><span data-stu-id="469fe-122">See how the chsh-game sample is rendered</span></span>](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

<span data-ttu-id="469fe-123">Esses metadados são fornecidos como um [cabeçalho YAML](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) que indica em quais idiomas sua amostra abrange (normalmente, isso será `qsharp` , `csharp` e `python` ) e quais produtos sua amostra cobre (normalmente, apenas `qdk` ).</span><span class="sxs-lookup"><span data-stu-id="469fe-123">This metadata is provided as a [YAML header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) that indicates what languages your sample covers (typically, this will be `qsharp`, `csharp`, and `python`), and what products your sample covers (typically, just `qdk`).</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> <span data-ttu-id="469fe-124">A `page_type: sample` chave no cabeçalho é necessária para que seu exemplo apareça em docs.Microsoft.com/Samples.</span><span class="sxs-lookup"><span data-stu-id="469fe-124">The `page_type: sample` key in the header is required for your sample to appear at docs.microsoft.com/samples.</span></span>
> <span data-ttu-id="469fe-125">Da mesma forma, as `product` `language` chaves e são críticas para ajudar os usuários a localizar e executar seu exemplo.</span><span class="sxs-lookup"><span data-stu-id="469fe-125">Similarly, the `product` and `language` keys are critical for helping users to find and run your sample.</span></span>

<span data-ttu-id="469fe-126">Depois disso, é útil dar uma breve introdução que diz o que o seu novo exemplo faz:</span><span class="sxs-lookup"><span data-stu-id="469fe-126">After that, it's helpful to give a short intro that says what your new sample does:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

<span data-ttu-id="469fe-127">Os usuários do seu exemplo também apreciarão saber o que precisam para executá-lo (por exemplo: os usuários precisam apenas do próprio kit de desenvolvimento Quantum ou precisam de software adicional, como node.js?):</span><span class="sxs-lookup"><span data-stu-id="469fe-127">Users of your sample will also appreciate knowing what they need to run it (e.g.: do users just need the Quantum Development Kit itself, or do they need additional software such as node.js?):</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

<span data-ttu-id="469fe-128">Com tudo em vigor, você pode dizer aos usuários como executar seu exemplo:</span><span class="sxs-lookup"><span data-stu-id="469fe-128">With all that in place, you can tell users how to run your sample:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

<span data-ttu-id="469fe-129">Por fim, é útil informar aos usuários o que cada arquivo do seu exemplo faz e onde eles podem ir para mais informações:</span><span class="sxs-lookup"><span data-stu-id="469fe-129">Finally, it's helpful to tell users what each file in your sample does, and where they can go for more information:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> <span data-ttu-id="469fe-130">Certifique-se de usar URLs absolutas aqui, pois seu exemplo será exibido em uma URL diferente quando renderizado em docs.microsoft.com/samples!</span><span class="sxs-lookup"><span data-stu-id="469fe-130">Make sure to use absolute URLs here, since your sample will appear at a different URL when rendered at docs.microsoft.com/samples!</span></span>
