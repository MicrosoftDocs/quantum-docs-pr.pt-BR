---
uid: Microsoft.Quantum.Arrays.IndexOf
title: Função IndexOf
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 7ff80f13f432a18f216b2dee4bd65b1e82034fa5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694460"
---
# <a name="indexof-function"></a><span data-ttu-id="e8e1c-102">Função IndexOf</span><span class="sxs-lookup"><span data-stu-id="e8e1c-102">IndexOf function</span></span>

<span data-ttu-id="e8e1c-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e8e1c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e8e1c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e8e1c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e8e1c-105">Retorna o primeiro índice do primeiro elemento em uma matriz que atende a um determinado predicado.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-105">Returns the first index of the first element in an array that satisfies a given predicate.</span></span> <span data-ttu-id="e8e1c-106">Se nenhum elemento desse tipo existir, retornará-1.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-106">If no such element exists, returns -1.</span></span>

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="e8e1c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8e1c-107">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="e8e1c-108">predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool</span><span class="sxs-lookup"><span data-stu-id="e8e1c-108">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e8e1c-109">Uma função de predicado agindo em elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-109">A predicate function acting on elements of the array.</span></span>


### <a name="arr--t"></a><span data-ttu-id="e8e1c-110">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="e8e1c-110">arr : 'T[]</span></span>

<span data-ttu-id="e8e1c-111">Uma matriz a ser pesquisada usando o predicado fornecido.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-111">An array to be searched using the given predicate.</span></span>



## <a name="output--int"></a><span data-ttu-id="e8e1c-112">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e8e1c-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e8e1c-113">O menor índice `idx` , como `predicate(arr[idx])` true, ou-1, se nenhum elemento desse tipo existir.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-113">Either the smallest index `idx` such that `predicate(arr[idx])` is true, or -1 if no such element exists.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e8e1c-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e8e1c-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e8e1c-115">T'</span><span class="sxs-lookup"><span data-stu-id="e8e1c-115">'T</span></span>

