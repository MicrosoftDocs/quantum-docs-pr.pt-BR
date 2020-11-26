---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Função não equalizador
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 4ac6cf4b220fa42c8eb946d6fbcad4cdb191afcd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197187"
---
# <a name="notequalr-function"></a><span data-ttu-id="94f53-102">Função não equalizador</span><span class="sxs-lookup"><span data-stu-id="94f53-102">NotEqualR function</span></span>

<span data-ttu-id="94f53-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="94f53-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="94f53-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="94f53-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="94f53-105">Retorna true se e somente se duas entradas não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="94f53-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="94f53-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="94f53-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="94f53-107">r: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="94f53-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="94f53-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="94f53-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="94f53-109">b: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="94f53-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="94f53-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="94f53-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="94f53-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="94f53-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="94f53-112">`true` se e somente se `a` não for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="94f53-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="94f53-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="94f53-113">Remarks</span></span>

<span data-ttu-id="94f53-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="94f53-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```