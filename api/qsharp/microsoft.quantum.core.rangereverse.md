---
uid: Microsoft.Quantum.Core.RangeReverse
title: Função RangeReverse
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: 7bd7c55abe0b56b9d30b4c6e91f7175101dd2948
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213830"
---
# <a name="rangereverse-function"></a><span data-ttu-id="49912-102">Função RangeReverse</span><span class="sxs-lookup"><span data-stu-id="49912-102">RangeReverse function</span></span>

<span data-ttu-id="49912-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="49912-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="49912-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="49912-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="49912-105">Retorna um novo intervalo que é o inverso do intervalo de entrada.</span><span class="sxs-lookup"><span data-stu-id="49912-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="49912-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="49912-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="49912-107">r: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="49912-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="49912-108">Intervalo de entrada.</span><span class="sxs-lookup"><span data-stu-id="49912-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="49912-109">Saída: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="49912-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="49912-110">Um novo intervalo que é o inverso do intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="49912-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="49912-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="49912-111">Remarks</span></span>

<span data-ttu-id="49912-112">Observe que o inverso de um intervalo não é simplesmente `end` .. `-step` . `start` , porque o último elemento real de um intervalo pode não ser o mesmo que `end` .</span><span class="sxs-lookup"><span data-stu-id="49912-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>