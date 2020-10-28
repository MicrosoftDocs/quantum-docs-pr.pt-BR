---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Função não equalizador
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 06615c7ffb6aafc296077990dfca0ce25e1e00fa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693097"
---
# <a name="notequalr-function"></a><span data-ttu-id="1511d-102">Função não equalizador</span><span class="sxs-lookup"><span data-stu-id="1511d-102">NotEqualR function</span></span>

<span data-ttu-id="1511d-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="1511d-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="1511d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1511d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1511d-105">Retorna true se e somente se duas entradas não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="1511d-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="1511d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1511d-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="1511d-107">r: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="1511d-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="1511d-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="1511d-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="1511d-109">b: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="1511d-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="1511d-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="1511d-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1511d-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1511d-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1511d-112">`true` se e somente se `a` não for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="1511d-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="1511d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1511d-113">Remarks</span></span>

<span data-ttu-id="1511d-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="1511d-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```