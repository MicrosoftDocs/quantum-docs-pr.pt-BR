---
uid: Microsoft.Quantum.Logical.LessThanOrEqualL
title: Função LessThanOrEqualL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualL
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 333b76fc4885104e107dd25003a4e0dd5a9dd4af
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693115"
---
# <a name="lessthanorequall-function"></a><span data-ttu-id="277dd-102">Função LessThanOrEqualL</span><span class="sxs-lookup"><span data-stu-id="277dd-102">LessThanOrEqualL function</span></span>

<span data-ttu-id="277dd-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="277dd-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="277dd-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="277dd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="277dd-105">Retornará true se e somente se um número for menor ou igual a outro número.</span><span class="sxs-lookup"><span data-stu-id="277dd-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="277dd-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="277dd-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="277dd-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="277dd-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="277dd-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="277dd-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="277dd-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="277dd-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="277dd-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="277dd-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="277dd-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="277dd-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="277dd-112">`true` se e somente se `a` for menor ou igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="277dd-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="277dd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="277dd-113">Remarks</span></span>

<span data-ttu-id="277dd-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="277dd-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualL(a, b);
```