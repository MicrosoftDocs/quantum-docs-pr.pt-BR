---
uid: Microsoft.Quantum.Core.RangeStart
title: Função RangeStart
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 3e4b0cebe34b4c98cb1d582a9cd11b46ff778517
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693579"
---
# <a name="rangestart-function"></a><span data-ttu-id="c7b20-102">Função RangeStart</span><span class="sxs-lookup"><span data-stu-id="c7b20-102">RangeStart function</span></span>

<span data-ttu-id="c7b20-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="c7b20-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="c7b20-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c7b20-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c7b20-105">Retorna o valor inicial definido do intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="c7b20-105">Returns the defined start value of the given range.</span></span>

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="c7b20-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7b20-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="c7b20-107">intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="c7b20-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="c7b20-108">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c7b20-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c7b20-109">O valor inicial definido do intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="c7b20-109">The defined start value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7b20-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7b20-110">Remarks</span></span>

<span data-ttu-id="c7b20-111">O primeiro elemento de uma expressão de intervalo é `start` , o segundo elemento é `start+step` , o terceiro elemento é `start+step+step` , etc., até que `end` seja passado.</span><span class="sxs-lookup"><span data-stu-id="c7b20-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="c7b20-112">Observe que o valor inicial definido de um intervalo é o mesmo que o primeiro elemento da sequência, a menos que o intervalo especifique uma sequência vazia (por exemplo, 2...</span><span class="sxs-lookup"><span data-stu-id="c7b20-112">Note that the defined start value of a range is the same as the first element of the sequence, unless the range specifies an empty sequence (for example, 2 ..</span></span> <span data-ttu-id="c7b20-113">1).</span><span class="sxs-lookup"><span data-stu-id="c7b20-113">1).</span></span>