---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Função enumerada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 94e8fdb7288bc43ed84d10a3292819b455a2be31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221412"
---
# <a name="enumerated-function"></a><span data-ttu-id="1dde5-102">Função enumerada</span><span class="sxs-lookup"><span data-stu-id="1dde5-102">Enumerated function</span></span>

<span data-ttu-id="1dde5-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1dde5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1dde5-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1dde5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1dde5-105">Dada uma matriz, retorna uma nova matriz contendo os elementos da matriz original junto com os índices de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="1dde5-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="1dde5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1dde5-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="1dde5-107">matriz: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="1dde5-107">array : 'TElement[]</span></span>

<span data-ttu-id="1dde5-108">Uma matriz cujos elementos devem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="1dde5-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="1dde5-109">Saída: ([int](xref:microsoft.quantum.lang-ref.int), ' TElement) []</span><span class="sxs-lookup"><span data-stu-id="1dde5-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="1dde5-110">Uma nova matriz que contém os elementos da matriz original junto com seus índices.</span><span class="sxs-lookup"><span data-stu-id="1dde5-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1dde5-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="1dde5-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="1dde5-112">'TElement</span><span class="sxs-lookup"><span data-stu-id="1dde5-112">'TElement</span></span>

<span data-ttu-id="1dde5-113">O tipo de elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="1dde5-113">The type of elements of the array.</span></span>