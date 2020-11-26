---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Função intercalada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 1ff5999cc19f47e3dcae601b960446923b613d90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220953"
---
# <a name="interleaved-function"></a><span data-ttu-id="28c9b-102">Função intercalada</span><span class="sxs-lookup"><span data-stu-id="28c9b-102">Interleaved function</span></span>

<span data-ttu-id="28c9b-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="28c9b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="28c9b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="28c9b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="28c9b-105">Intercala duas matrizes de (quase) mesmo tamanho.</span><span class="sxs-lookup"><span data-stu-id="28c9b-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="28c9b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="28c9b-106">Description</span></span>

<span data-ttu-id="28c9b-107">Essa função retorna a intercalação de duas matrizes, começando com o primeiro elemento da primeira matriz, depois o primeiro elemento da segunda matriz e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="28c9b-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="28c9b-108">A primeira matriz deve ser do mesmo comprimento que a segunda, ou pode ter mais um elemento.</span><span class="sxs-lookup"><span data-stu-id="28c9b-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="28c9b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="28c9b-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="28c9b-110">Primeiro: ' t []</span><span class="sxs-lookup"><span data-stu-id="28c9b-110">first : 'T[]</span></span>

<span data-ttu-id="28c9b-111">A primeira matriz a ser intercalada.</span><span class="sxs-lookup"><span data-stu-id="28c9b-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="28c9b-112">Segundo: ' t []</span><span class="sxs-lookup"><span data-stu-id="28c9b-112">second : 'T[]</span></span>

<span data-ttu-id="28c9b-113">A segunda matriz a ser intercalada.</span><span class="sxs-lookup"><span data-stu-id="28c9b-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="28c9b-114">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="28c9b-114">Output : 'T[]</span></span>

<span data-ttu-id="28c9b-115">Matriz intercalada</span><span class="sxs-lookup"><span data-stu-id="28c9b-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="28c9b-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="28c9b-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="28c9b-117">T'</span><span class="sxs-lookup"><span data-stu-id="28c9b-117">'T</span></span>

<span data-ttu-id="28c9b-118">O tipo de cada elemento de `first` e `second` .</span><span class="sxs-lookup"><span data-stu-id="28c9b-118">The type of each element of `first` and `second`.</span></span>