---
uid: Microsoft.Quantum.Logical.EqualR
title: Função Equals
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 5aaa17303d75b27c3ac82cbe7d739a60016fdcb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693131"
---
# <a name="equalr-function"></a><span data-ttu-id="2a383-102">Função Equals</span><span class="sxs-lookup"><span data-stu-id="2a383-102">EqualR function</span></span>

<span data-ttu-id="2a383-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2a383-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2a383-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2a383-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2a383-105">Retorna true se e somente se duas entradas forem iguais.</span><span class="sxs-lookup"><span data-stu-id="2a383-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="2a383-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a383-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="2a383-107">r: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="2a383-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="2a383-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="2a383-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="2a383-109">b: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="2a383-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="2a383-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="2a383-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2a383-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2a383-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2a383-112">`true` se e somente se `a` for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="2a383-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a383-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a383-113">Remarks</span></span>

<span data-ttu-id="2a383-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="2a383-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```