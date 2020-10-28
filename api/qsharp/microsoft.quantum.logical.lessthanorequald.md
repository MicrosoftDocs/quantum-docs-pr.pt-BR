---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: Função LessThanOrEqualD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 7b0e9da379bd67eb78a80e7a535a15dcb8ba85c7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693119"
---
# <a name="lessthanorequald-function"></a><span data-ttu-id="17f9a-102">Função LessThanOrEqualD</span><span class="sxs-lookup"><span data-stu-id="17f9a-102">LessThanOrEqualD function</span></span>

<span data-ttu-id="17f9a-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="17f9a-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="17f9a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="17f9a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="17f9a-105">Retornará true se e somente se um número for menor ou igual a outro número.</span><span class="sxs-lookup"><span data-stu-id="17f9a-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="17f9a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="17f9a-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="17f9a-107">r: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="17f9a-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="17f9a-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="17f9a-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="17f9a-109">b: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="17f9a-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="17f9a-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="17f9a-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="17f9a-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="17f9a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="17f9a-112">`true` se e somente se `a` for menor ou igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="17f9a-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="17f9a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="17f9a-113">Remarks</span></span>

<span data-ttu-id="17f9a-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="17f9a-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```