---
uid: Microsoft.Quantum.Logical.NotEqualL
title: Função não Equals
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualL
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: f1d36c284293519e75e6c30ac64679c7bdf4609c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693099"
---
# <a name="notequall-function"></a><span data-ttu-id="2e963-102">Função não Equals</span><span class="sxs-lookup"><span data-stu-id="2e963-102">NotEqualL function</span></span>

<span data-ttu-id="2e963-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2e963-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2e963-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2e963-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2e963-105">Retorna true se e somente se duas entradas não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="2e963-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="2e963-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e963-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="2e963-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2e963-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2e963-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="2e963-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="2e963-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2e963-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2e963-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="2e963-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2e963-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2e963-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2e963-112">`true` se e somente se `a` não for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="2e963-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e963-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e963-113">Remarks</span></span>

<span data-ttu-id="2e963-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="2e963-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualL(a, b);
```