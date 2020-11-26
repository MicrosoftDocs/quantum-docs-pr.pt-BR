---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Função IndexRange
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 5afd4cc260ac3e384d2736bf7b43d941afd9ef73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220936"
---
# <a name="indexrange-function"></a><span data-ttu-id="32e3a-102">Função IndexRange</span><span class="sxs-lookup"><span data-stu-id="32e3a-102">IndexRange function</span></span>

<span data-ttu-id="32e3a-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="32e3a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="32e3a-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="32e3a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="32e3a-105">Dada uma matriz, retorna um intervalo sobre os índices dessa matriz, adequado para uso em um loop for.</span><span class="sxs-lookup"><span data-stu-id="32e3a-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="32e3a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="32e3a-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="32e3a-107">matriz: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="32e3a-107">array : 'TElement[]</span></span>

<span data-ttu-id="32e3a-108">Uma matriz para a qual um intervalo de índices deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="32e3a-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="32e3a-109">Saída: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="32e3a-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="32e3a-110">Um intervalo em todos os índices da matriz.</span><span class="sxs-lookup"><span data-stu-id="32e3a-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="32e3a-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="32e3a-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="32e3a-112">'TElement</span><span class="sxs-lookup"><span data-stu-id="32e3a-112">'TElement</span></span>

<span data-ttu-id="32e3a-113">O tipo de elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="32e3a-113">The type of elements of the array.</span></span>