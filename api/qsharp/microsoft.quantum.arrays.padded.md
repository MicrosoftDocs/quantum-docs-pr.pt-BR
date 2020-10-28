---
uid: Microsoft.Quantum.Arrays.Padded
title: Função preenchida
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 8742d4726e7ee32349bf3d0bd5077352ffca350b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694428"
---
# <a name="padded-function"></a><span data-ttu-id="fd093-102">Função preenchida</span><span class="sxs-lookup"><span data-stu-id="fd093-102">Padded function</span></span>

<span data-ttu-id="fd093-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="fd093-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="fd093-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fd093-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fd093-105">Retorna uma matriz preenchida com valores especificados até um comprimento especificado.</span><span class="sxs-lookup"><span data-stu-id="fd093-105">Returns an array padded at with specified values up to a specified length.</span></span>

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="fd093-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd093-106">Input</span></span>

### <a name="nelementstotal--int"></a><span data-ttu-id="fd093-107">nElementsTotal: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fd093-107">nElementsTotal : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fd093-108">O comprimento da matriz preenchida.</span><span class="sxs-lookup"><span data-stu-id="fd093-108">The length of the padded array.</span></span> <span data-ttu-id="fd093-109">Se isso for positivo, `inputArray` será preenchido no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="fd093-109">If this is positive, `inputArray` is padded at the head.</span></span> <span data-ttu-id="fd093-110">Se isso for negativo, `inputArray` será preenchido na parte final.</span><span class="sxs-lookup"><span data-stu-id="fd093-110">If this is negative, `inputArray` is padded at the tail.</span></span>


### <a name="defaultelement--t"></a><span data-ttu-id="fd093-111">padrão: ' t</span><span class="sxs-lookup"><span data-stu-id="fd093-111">defaultElement : 'T</span></span>

<span data-ttu-id="fd093-112">Valor padrão a ser usado para elementos de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="fd093-112">Default value to use for padding elements.</span></span>


### <a name="inputarray--t"></a><span data-ttu-id="fd093-113">inputArray: ' t []</span><span class="sxs-lookup"><span data-stu-id="fd093-113">inputArray : 'T[]</span></span>

<span data-ttu-id="fd093-114">Matriz cujos valores estão no início da matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="fd093-114">Array whose values are at the head of the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="fd093-115">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="fd093-115">Output : 'T[]</span></span>

<span data-ttu-id="fd093-116">Uma matriz `output` que é `inputArray` preenchida na cabeça com `defaultElement` s até o `output` comprimento `nElementsTotal`</span><span class="sxs-lookup"><span data-stu-id="fd093-116">An array `output` that is the `inputArray` padded at the head with `defaultElement`s until `output` has length `nElementsTotal`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fd093-117">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="fd093-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fd093-118">T'</span><span class="sxs-lookup"><span data-stu-id="fd093-118">'T</span></span>

<span data-ttu-id="fd093-119">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="fd093-119">The type of the array elements.</span></span>