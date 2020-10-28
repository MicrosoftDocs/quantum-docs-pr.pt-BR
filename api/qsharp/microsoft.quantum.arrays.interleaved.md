---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Função intercalada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 8405cabca17f2dd7c2680833bfab5c3768fcf752
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694455"
---
# <a name="interleaved-function"></a><span data-ttu-id="5d67d-102">Função intercalada</span><span class="sxs-lookup"><span data-stu-id="5d67d-102">Interleaved function</span></span>

<span data-ttu-id="5d67d-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5d67d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5d67d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5d67d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5d67d-105">Intercala duas matrizes de (quase) mesmo tamanho.</span><span class="sxs-lookup"><span data-stu-id="5d67d-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="5d67d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d67d-106">Description</span></span>

<span data-ttu-id="5d67d-107">Essa função retorna a intercalação de duas matrizes, começando com o primeiro elemento da primeira matriz, depois o primeiro elemento da segunda matriz e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5d67d-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="5d67d-108">A primeira matriz deve ser do mesmo comprimento que a segunda, ou pode ter mais um elemento.</span><span class="sxs-lookup"><span data-stu-id="5d67d-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="5d67d-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="5d67d-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="5d67d-110">Primeiro: ' t []</span><span class="sxs-lookup"><span data-stu-id="5d67d-110">first : 'T[]</span></span>

<span data-ttu-id="5d67d-111">A primeira matriz a ser intercalada.</span><span class="sxs-lookup"><span data-stu-id="5d67d-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="5d67d-112">Segundo: ' t []</span><span class="sxs-lookup"><span data-stu-id="5d67d-112">second : 'T[]</span></span>

<span data-ttu-id="5d67d-113">A segunda matriz a ser intercalada.</span><span class="sxs-lookup"><span data-stu-id="5d67d-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="5d67d-114">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="5d67d-114">Output : 'T[]</span></span>

<span data-ttu-id="5d67d-115">Matriz intercalada</span><span class="sxs-lookup"><span data-stu-id="5d67d-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5d67d-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="5d67d-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5d67d-117">T'</span><span class="sxs-lookup"><span data-stu-id="5d67d-117">'T</span></span>

<span data-ttu-id="5d67d-118">O tipo de cada elemento de `first` e `second` .</span><span class="sxs-lookup"><span data-stu-id="5d67d-118">The type of each element of `first` and `second`.</span></span>