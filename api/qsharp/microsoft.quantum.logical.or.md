---
uid: Microsoft.Quantum.Logical.Or
title: Função or
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 98a416229386461b241d087b7ae95f078f8be70a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694594"
---
# <a name="or-function"></a><span data-ttu-id="4796e-102">Função or</span><span class="sxs-lookup"><span data-stu-id="4796e-102">Or function</span></span>

<span data-ttu-id="4796e-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="4796e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="4796e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4796e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4796e-105">Retorna a disjunção booliana de dois valores.</span><span class="sxs-lookup"><span data-stu-id="4796e-105">Returns the Boolean disjunction of two values.</span></span>

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="4796e-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4796e-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="4796e-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4796e-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4796e-108">O primeiro valor a ser considerado.</span><span class="sxs-lookup"><span data-stu-id="4796e-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="4796e-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4796e-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4796e-110">O segundo valor a ser considerado.</span><span class="sxs-lookup"><span data-stu-id="4796e-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="4796e-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4796e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4796e-112">`true` se e somente se o `a` `b` for ou for `true` .</span><span class="sxs-lookup"><span data-stu-id="4796e-112">`true` if and only if either `a` or `b` are `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="4796e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4796e-113">Remarks</span></span>

<span data-ttu-id="4796e-114">Ao contrário do `or` operador, essa função não é de curto circuito, de modo que ambas as entradas são totalmente avaliadas.</span><span class="sxs-lookup"><span data-stu-id="4796e-114">Unlike the `or` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="4796e-115">Até o comportamento de curto-circuito, os seguintes são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="4796e-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a or b;
let x = Or(a, b);
```