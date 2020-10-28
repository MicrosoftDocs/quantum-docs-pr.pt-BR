---
uid: Microsoft.Quantum.Core.RangeReverse
title: Função RangeReverse
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: d4e612d2f175015b7193634aeec12f9df12df7d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693588"
---
# <a name="rangereverse-function"></a><span data-ttu-id="e8971-102">Função RangeReverse</span><span class="sxs-lookup"><span data-stu-id="e8971-102">RangeReverse function</span></span>

<span data-ttu-id="e8971-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="e8971-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="e8971-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e8971-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e8971-105">Retorna um novo intervalo que é o inverso do intervalo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e8971-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="e8971-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8971-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="e8971-107">r: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="e8971-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="e8971-108">Intervalo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e8971-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="e8971-109">Saída: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="e8971-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="e8971-110">Um novo intervalo que é o inverso do intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="e8971-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8971-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8971-111">Remarks</span></span>

<span data-ttu-id="e8971-112">Observe que o inverso de um intervalo não é simplesmente `end` .. `-step` . `start` , porque o último elemento real de um intervalo pode não ser o mesmo que `end` .</span><span class="sxs-lookup"><span data-stu-id="e8971-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>