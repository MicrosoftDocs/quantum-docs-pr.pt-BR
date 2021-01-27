---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Função enumerada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: adb13d8b25c9e4a6011ade119ffa3cb2783f60e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848135"
---
# <a name="enumerated-function"></a><span data-ttu-id="e82c9-102">Função enumerada</span><span class="sxs-lookup"><span data-stu-id="e82c9-102">Enumerated function</span></span>

<span data-ttu-id="e82c9-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e82c9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e82c9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e82c9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e82c9-105">Dada uma matriz, retorna uma nova matriz contendo os elementos da matriz original junto com os índices de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="e82c9-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="e82c9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e82c9-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="e82c9-107">matriz: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="e82c9-107">array : 'TElement[]</span></span>

<span data-ttu-id="e82c9-108">Uma matriz cujos elementos devem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="e82c9-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="e82c9-109">Saída: ([int](xref:microsoft.quantum.lang-ref.int), ' TElement) []</span><span class="sxs-lookup"><span data-stu-id="e82c9-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="e82c9-110">Uma nova matriz que contém os elementos da matriz original junto com seus índices.</span><span class="sxs-lookup"><span data-stu-id="e82c9-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e82c9-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e82c9-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="e82c9-112">'TElement</span><span class="sxs-lookup"><span data-stu-id="e82c9-112">'TElement</span></span>

<span data-ttu-id="e82c9-113">O tipo de elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="e82c9-113">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="e82c9-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e82c9-114">Example</span></span>

<span data-ttu-id="e82c9-115">Os seguintes `for` loops são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="e82c9-115">The following `for` loops are equivalent:</span></span>

```qsharp
for (idx in IndexRange(array)) {
    let element = array[idx];
    ...
}
for ((idx, element) in Enumerated(array)) { ... }
```