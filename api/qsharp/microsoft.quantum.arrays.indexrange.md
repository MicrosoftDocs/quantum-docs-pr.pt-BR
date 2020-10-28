---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Função IndexRange
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 7f9779acd4a781c50388217aa780710bd0b99ff3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694456"
---
# <a name="indexrange-function"></a><span data-ttu-id="ae76f-102">Função IndexRange</span><span class="sxs-lookup"><span data-stu-id="ae76f-102">IndexRange function</span></span>

<span data-ttu-id="ae76f-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ae76f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ae76f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ae76f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ae76f-105">Dada uma matriz, retorna um intervalo sobre os índices dessa matriz, adequado para uso em um loop for.</span><span class="sxs-lookup"><span data-stu-id="ae76f-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="ae76f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ae76f-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="ae76f-107">matriz: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="ae76f-107">array : 'TElement[]</span></span>

<span data-ttu-id="ae76f-108">Uma matriz para a qual um intervalo de índices deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="ae76f-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="ae76f-109">Saída: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="ae76f-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="ae76f-110">Um intervalo em todos os índices da matriz.</span><span class="sxs-lookup"><span data-stu-id="ae76f-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ae76f-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ae76f-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="ae76f-112">'TElement</span><span class="sxs-lookup"><span data-stu-id="ae76f-112">'TElement</span></span>

<span data-ttu-id="ae76f-113">O tipo de elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="ae76f-113">The type of elements of the array.</span></span>