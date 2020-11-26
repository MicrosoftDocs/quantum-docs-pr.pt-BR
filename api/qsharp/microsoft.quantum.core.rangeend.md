---
uid: Microsoft.Quantum.Core.RangeEnd
title: Função RangeEnd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 90a9e31bf5c4a5e92a35998ddaec8c9e9de9888e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224030"
---
# <a name="rangeend-function"></a><span data-ttu-id="fb7d6-102">Função RangeEnd</span><span class="sxs-lookup"><span data-stu-id="fb7d6-102">RangeEnd function</span></span>

<span data-ttu-id="fb7d6-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="fb7d6-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="fb7d6-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="fb7d6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="fb7d6-105">Retorna o valor final definido do intervalo especificado, que não é necessariamente o último elemento na sequência.</span><span class="sxs-lookup"><span data-stu-id="fb7d6-105">Returns the defined end value of the given range, which is not necessarily the last element in the sequence.</span></span>

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="fb7d6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb7d6-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="fb7d6-107">intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="fb7d6-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="fb7d6-108">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fb7d6-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fb7d6-109">O valor final definido do intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="fb7d6-109">The defined end value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb7d6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb7d6-110">Remarks</span></span>

<span data-ttu-id="fb7d6-111">O primeiro elemento de uma expressão de intervalo é `start` , o segundo elemento é `start+step` , o terceiro elemento é `start+step+step` , etc., até que `end` seja passado.</span><span class="sxs-lookup"><span data-stu-id="fb7d6-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="fb7d6-112">Observe que o valor final definido de um intervalo pode ser diferente do último elemento na sequência especificada pelo intervalo; por exemplo, em um intervalo de 0..</span><span class="sxs-lookup"><span data-stu-id="fb7d6-112">Note that the defined end value of a range can differ from the last element in the sequence specified by the range; for example, in a range 0 ..</span></span> <span data-ttu-id="fb7d6-113">2..</span><span class="sxs-lookup"><span data-stu-id="fb7d6-113">2 ..</span></span> <span data-ttu-id="fb7d6-114">5 o último elemento é 4, mas o valor final é 5.</span><span class="sxs-lookup"><span data-stu-id="fb7d6-114">5 the last element is 4 but the end value is 5.</span></span>