---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Função IndexRange
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 043b56a1ac3cbe5cd59cdd45d3725f301d81a6ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845791"
---
# <a name="indexrange-function"></a><span data-ttu-id="10e2b-102">Função IndexRange</span><span class="sxs-lookup"><span data-stu-id="10e2b-102">IndexRange function</span></span>

<span data-ttu-id="10e2b-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="10e2b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="10e2b-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="10e2b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="10e2b-105">Dada uma matriz, retorna um intervalo sobre os índices dessa matriz, adequado para uso em um loop for.</span><span class="sxs-lookup"><span data-stu-id="10e2b-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="10e2b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="10e2b-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="10e2b-107">matriz: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="10e2b-107">array : 'TElement[]</span></span>

<span data-ttu-id="10e2b-108">Uma matriz para a qual um intervalo de índices deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="10e2b-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="10e2b-109">Saída: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="10e2b-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="10e2b-110">Um intervalo em todos os índices da matriz.</span><span class="sxs-lookup"><span data-stu-id="10e2b-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="10e2b-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="10e2b-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="10e2b-112">'TElement</span><span class="sxs-lookup"><span data-stu-id="10e2b-112">'TElement</span></span>

<span data-ttu-id="10e2b-113">O tipo de elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="10e2b-113">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="10e2b-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="10e2b-114">Example</span></span>

<span data-ttu-id="10e2b-115">Os seguintes `for` loops são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="10e2b-115">The following `for` loops are equivalent:</span></span>

```qsharp
for (idx in IndexRange(array)) { ... }
for (idx in IndexRange(array)) { ... }
```