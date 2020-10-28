---
uid: Microsoft.Quantum.Logical.EqualB
title: Função EqualB
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 91ab51180018a9b95a2f9010477c0a24f3a54617
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694728"
---
# <a name="equalb-function"></a><span data-ttu-id="04ba5-102">Função EqualB</span><span class="sxs-lookup"><span data-stu-id="04ba5-102">EqualB function</span></span>

<span data-ttu-id="04ba5-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="04ba5-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="04ba5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="04ba5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="04ba5-105">Retorna true se e somente se duas entradas forem iguais.</span><span class="sxs-lookup"><span data-stu-id="04ba5-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="04ba5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="04ba5-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="04ba5-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="04ba5-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="04ba5-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="04ba5-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="04ba5-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="04ba5-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="04ba5-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="04ba5-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="04ba5-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="04ba5-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="04ba5-112">`true` se e somente se `a` for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="04ba5-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="04ba5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="04ba5-113">Remarks</span></span>

<span data-ttu-id="04ba5-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="04ba5-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualB(a, b);
```