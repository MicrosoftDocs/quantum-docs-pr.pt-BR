---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: Função CumulativeFolded
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: ffb934d06f6be06cbc35a523c90d2c54e0a51353
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210022"
---
# <a name="cumulativefolded-function"></a><span data-ttu-id="a7fae-102">Função CumulativeFolded</span><span class="sxs-lookup"><span data-stu-id="a7fae-102">CumulativeFolded function</span></span>

<span data-ttu-id="a7fae-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a7fae-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a7fae-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a7fae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a7fae-105">Combina mapeadas e dobras em uma única função</span><span class="sxs-lookup"><span data-stu-id="a7fae-105">Combines Mapped and Fold into a single function</span></span>

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a><span data-ttu-id="a7fae-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7fae-106">Description</span></span>

<span data-ttu-id="a7fae-107">Essa função itera a `fn` função por meio da matriz, começando a partir de um estado inicial `state` e retorna todos os valores intermediários, não incluindo o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="a7fae-107">This function iterates the `fn` function through the array, starting from an initial state `state` and returns all intermediate values, not including the inital state.</span></span>

## <a name="input"></a><span data-ttu-id="a7fae-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7fae-108">Input</span></span>

### <a name="fn--statet---state"></a><span data-ttu-id="a7fae-109">FN: (' State, ' t)-estado de ></span><span class="sxs-lookup"><span data-stu-id="a7fae-109">fn : ('State,'T) -> 'State</span></span>

<span data-ttu-id="a7fae-110">Uma função a ser dobrada sobre a matriz</span><span class="sxs-lookup"><span data-stu-id="a7fae-110">A function to be folded over the array</span></span>


### <a name="state--state"></a><span data-ttu-id="a7fae-111">Estado: ' estado</span><span class="sxs-lookup"><span data-stu-id="a7fae-111">state : 'State</span></span>

<span data-ttu-id="a7fae-112">O estado inicial a ser dobrado</span><span class="sxs-lookup"><span data-stu-id="a7fae-112">The initial state to be folded</span></span>


### <a name="array--t"></a><span data-ttu-id="a7fae-113">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="a7fae-113">array : 'T[]</span></span>

<span data-ttu-id="a7fae-114">Uma matriz de valores a serem dobrados</span><span class="sxs-lookup"><span data-stu-id="a7fae-114">An array of values to be folded over</span></span>



## <a name="output--state"></a><span data-ttu-id="a7fae-115">Saída: ' State []</span><span class="sxs-lookup"><span data-stu-id="a7fae-115">Output : 'State[]</span></span>

<span data-ttu-id="a7fae-116">Todos os Estados intermediários, incluindo o estado final, mas não o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="a7fae-116">All intermediate states, including the final state, but not the initial state.</span></span>
<span data-ttu-id="a7fae-117">O comprimento da matriz de saída é do mesmo comprimento que `array` .</span><span class="sxs-lookup"><span data-stu-id="a7fae-117">The length of the output array is of the same length as `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a7fae-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a7fae-118">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="a7fae-119">' Estado</span><span class="sxs-lookup"><span data-stu-id="a7fae-119">'State</span></span>

<span data-ttu-id="a7fae-120">O tipo de estado no qual a `fn` função Opera, ou seja, aceita como sua primeira entrada e retorna.</span><span class="sxs-lookup"><span data-stu-id="a7fae-120">The type of states that the `fn` function operates on, i.e., accepts as its first input and returns.</span></span>
### <a name="t"></a><span data-ttu-id="a7fae-121">T'</span><span class="sxs-lookup"><span data-stu-id="a7fae-121">'T</span></span>

<span data-ttu-id="a7fae-122">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="a7fae-122">The type of `array` elements.</span></span>