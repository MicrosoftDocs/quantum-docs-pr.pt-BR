---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Operação MaybeChooseElement
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 86a69110fc92a2b6238cc757c09185c9fbcdb035
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856126"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="650a6-102">Operação MaybeChooseElement</span><span class="sxs-lookup"><span data-stu-id="650a6-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="650a6-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="650a6-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="650a6-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="650a6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="650a6-105">Dada uma matriz de dados e uma distribuição sobre seus índices, o tenta escolher um elemento aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="650a6-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="650a6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="650a6-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="650a6-107">dados: ' t []</span><span class="sxs-lookup"><span data-stu-id="650a6-107">data : 'T[]</span></span>

<span data-ttu-id="650a6-108">A matriz da qual um elemento deve ser escolhido.</span><span class="sxs-lookup"><span data-stu-id="650a6-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="650a6-109">indexDistribution: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="650a6-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="650a6-110">Uma distribuição nos índices de `data` .</span><span class="sxs-lookup"><span data-stu-id="650a6-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="650a6-111">Saída: ([bool](xref:microsoft.quantum.lang-ref.bool), não)</span><span class="sxs-lookup"><span data-stu-id="650a6-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="650a6-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="650a6-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="650a6-113">T'</span><span class="sxs-lookup"><span data-stu-id="650a6-113">'T</span></span>



## <a name="example"></a><span data-ttu-id="650a6-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="650a6-114">Example</span></span>

<span data-ttu-id="650a6-115">O trecho de código Q # a seguir escolhe um elemento aleatoriamente de uma matriz:</span><span class="sxs-lookup"><span data-stu-id="650a6-115">The following Q# snippet chooses an element at random from an array:</span></span>

```qsharp
let (succeeded, element) = MaybeChooseElement(
    data,
    DiscreteUniformDistribution(0, Length(data) - 1)
);
Fact(succeeded, "Index chosen by MaybeChooseElement was not valid.");
```