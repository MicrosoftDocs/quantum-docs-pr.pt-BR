---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Função enumerada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 0a591025a4eef79e08b47527c0bdb556f5645334
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694482"
---
# <a name="enumerated-function"></a><span data-ttu-id="677d9-102">Função enumerada</span><span class="sxs-lookup"><span data-stu-id="677d9-102">Enumerated function</span></span>

<span data-ttu-id="677d9-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="677d9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="677d9-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="677d9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="677d9-105">Dada uma matriz, retorna uma nova matriz contendo os elementos da matriz original junto com os índices de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="677d9-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="677d9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="677d9-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="677d9-107">matriz: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="677d9-107">array : 'TElement[]</span></span>

<span data-ttu-id="677d9-108">Uma matriz cujos elementos devem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="677d9-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="677d9-109">Saída: ([int](xref:microsoft.quantum.lang-ref.int), ' TElement) []</span><span class="sxs-lookup"><span data-stu-id="677d9-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="677d9-110">Uma nova matriz que contém os elementos da matriz original junto com seus índices.</span><span class="sxs-lookup"><span data-stu-id="677d9-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="677d9-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="677d9-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="677d9-112">'TElement</span><span class="sxs-lookup"><span data-stu-id="677d9-112">'TElement</span></span>

<span data-ttu-id="677d9-113">O tipo de elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="677d9-113">The type of elements of the array.</span></span>