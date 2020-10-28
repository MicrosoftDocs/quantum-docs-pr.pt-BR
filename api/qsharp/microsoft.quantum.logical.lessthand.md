---
uid: Microsoft.Quantum.Logical.LessThanD
title: Função LessThanD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 8cd274d5e299df2f556006baf7457d54aebcd071
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696807"
---
# <a name="lessthand-function"></a><span data-ttu-id="699b6-102">Função LessThanD</span><span class="sxs-lookup"><span data-stu-id="699b6-102">LessThanD function</span></span>

<span data-ttu-id="699b6-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="699b6-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="699b6-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="699b6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="699b6-105">Retorna true se e somente se um número for menor que outro número.</span><span class="sxs-lookup"><span data-stu-id="699b6-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="699b6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="699b6-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="699b6-107">r: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="699b6-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="699b6-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="699b6-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="699b6-109">b: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="699b6-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="699b6-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="699b6-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="699b6-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="699b6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="699b6-112">`true` se e somente se `a` for estritamente menor que `b` .</span><span class="sxs-lookup"><span data-stu-id="699b6-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="699b6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="699b6-113">Remarks</span></span>

<span data-ttu-id="699b6-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="699b6-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanD(a, b);
```