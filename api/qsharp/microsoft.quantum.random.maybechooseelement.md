---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Operação MaybeChooseElement
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 12640d9dc3aad301146eff7bcbbaae33d3ccd420
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694948"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="cf01d-102">Operação MaybeChooseElement</span><span class="sxs-lookup"><span data-stu-id="cf01d-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="cf01d-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="cf01d-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="cf01d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cf01d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cf01d-105">Dada uma matriz de dados e uma distribuição sobre seus índices, o tenta escolher um elemento aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="cf01d-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="cf01d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="cf01d-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="cf01d-107">dados: ' t []</span><span class="sxs-lookup"><span data-stu-id="cf01d-107">data : 'T[]</span></span>

<span data-ttu-id="cf01d-108">A matriz da qual um elemento deve ser escolhido.</span><span class="sxs-lookup"><span data-stu-id="cf01d-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="cf01d-109">indexDistribution: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="cf01d-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="cf01d-110">Uma distribuição nos índices de `data` .</span><span class="sxs-lookup"><span data-stu-id="cf01d-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="cf01d-111">Saída: ([bool](xref:microsoft.quantum.lang-ref.bool), não)</span><span class="sxs-lookup"><span data-stu-id="cf01d-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cf01d-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="cf01d-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cf01d-113">T'</span><span class="sxs-lookup"><span data-stu-id="cf01d-113">'T</span></span>
