---
uid: Microsoft.Quantum.Logical.EqualL
title: Função de igual
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: f0a2bfa866068746e9c6e249573eb61c0d08c0f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693132"
---
# <a name="equall-function"></a><span data-ttu-id="856cb-102">Função de igual</span><span class="sxs-lookup"><span data-stu-id="856cb-102">EqualL function</span></span>

<span data-ttu-id="856cb-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="856cb-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="856cb-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="856cb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="856cb-105">Retorna true se e somente se duas entradas forem iguais.</span><span class="sxs-lookup"><span data-stu-id="856cb-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="856cb-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="856cb-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="856cb-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="856cb-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="856cb-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="856cb-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="856cb-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="856cb-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="856cb-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="856cb-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="856cb-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="856cb-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="856cb-112">`true` se e somente se `a` for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="856cb-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="856cb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="856cb-113">Remarks</span></span>

<span data-ttu-id="856cb-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="856cb-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualL(a, b);
```