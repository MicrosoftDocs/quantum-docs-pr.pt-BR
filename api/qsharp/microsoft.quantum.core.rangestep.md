---
uid: Microsoft.Quantum.Core.RangeStep
title: Função RangeStep
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: 39c8581fe795a1b76d2a6e81c238a271287c2c38
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213796"
---
# <a name="rangestep-function"></a><span data-ttu-id="56935-102">Função RangeStep</span><span class="sxs-lookup"><span data-stu-id="56935-102">RangeStep function</span></span>

<span data-ttu-id="56935-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="56935-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="56935-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="56935-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="56935-105">Retorna o inteiro que especifica como o próximo valor de um intervalo é calculado.</span><span class="sxs-lookup"><span data-stu-id="56935-105">Returns the integer that specifies how the next value of a range is calculated.</span></span>

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="56935-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="56935-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="56935-107">intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="56935-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="56935-108">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="56935-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="56935-109">O valor de etapa definido do intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="56935-109">The defined step value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="56935-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="56935-110">Remarks</span></span>

<span data-ttu-id="56935-111">O primeiro elemento de uma expressão de intervalo é `start` , o segundo elemento é `start+step` , o terceiro elemento é `start+step+step` , etc., até que `end` seja passado.</span><span class="sxs-lookup"><span data-stu-id="56935-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>