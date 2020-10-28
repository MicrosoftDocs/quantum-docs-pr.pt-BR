---
uid: Microsoft.Quantum.Core.RangeEnd
title: Função RangeEnd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 4dbcf517c4dc17775040444c77deb0e449082390
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693590"
---
# <a name="rangeend-function"></a><span data-ttu-id="f15a8-102">Função RangeEnd</span><span class="sxs-lookup"><span data-stu-id="f15a8-102">RangeEnd function</span></span>

<span data-ttu-id="f15a8-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="f15a8-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="f15a8-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f15a8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f15a8-105">Retorna o valor final definido do intervalo especificado, que não é necessariamente o último elemento na sequência.</span><span class="sxs-lookup"><span data-stu-id="f15a8-105">Returns the defined end value of the given range, which is not necessarily the last element in the sequence.</span></span>

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="f15a8-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f15a8-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="f15a8-107">intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="f15a8-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="f15a8-108">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f15a8-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f15a8-109">O valor final definido do intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="f15a8-109">The defined end value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="f15a8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f15a8-110">Remarks</span></span>

<span data-ttu-id="f15a8-111">O primeiro elemento de uma expressão de intervalo é `start` , o segundo elemento é `start+step` , o terceiro elemento é `start+step+step` , etc., até que `end` seja passado.</span><span class="sxs-lookup"><span data-stu-id="f15a8-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="f15a8-112">Observe que o valor final definido de um intervalo pode ser diferente do último elemento na sequência especificada pelo intervalo; por exemplo, em um intervalo de 0..</span><span class="sxs-lookup"><span data-stu-id="f15a8-112">Note that the defined end value of a range can differ from the last element in the sequence specified by the range; for example, in a range 0 ..</span></span> <span data-ttu-id="f15a8-113">2..</span><span class="sxs-lookup"><span data-stu-id="f15a8-113">2 ..</span></span> <span data-ttu-id="f15a8-114">5 o último elemento é 4, mas o valor final é 5.</span><span class="sxs-lookup"><span data-stu-id="f15a8-114">5 the last element is 4 but the end value is 5.</span></span>