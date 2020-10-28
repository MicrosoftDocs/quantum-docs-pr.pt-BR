---
uid: Microsoft.Quantum.Logical.And
title: Função and
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: cc81f650216c4db219a79c4fe89a42447a4e95b8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694731"
---
# <a name="and-function"></a><span data-ttu-id="9313c-102">Função and</span><span class="sxs-lookup"><span data-stu-id="9313c-102">And function</span></span>

<span data-ttu-id="9313c-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="9313c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="9313c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9313c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9313c-105">Retorna a conjunção booliana de dois valores.</span><span class="sxs-lookup"><span data-stu-id="9313c-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="9313c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="9313c-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="9313c-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9313c-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9313c-108">O primeiro valor a ser considerado.</span><span class="sxs-lookup"><span data-stu-id="9313c-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="9313c-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9313c-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9313c-110">O segundo valor a ser considerado.</span><span class="sxs-lookup"><span data-stu-id="9313c-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9313c-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9313c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9313c-112">`true` se e somente se `a` e `b` forem ambos `true` .</span><span class="sxs-lookup"><span data-stu-id="9313c-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9313c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9313c-113">Remarks</span></span>

<span data-ttu-id="9313c-114">Ao contrário do `and` operador, essa função não é de curto circuito, de modo que ambas as entradas são totalmente avaliadas.</span><span class="sxs-lookup"><span data-stu-id="9313c-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="9313c-115">Até o comportamento de curto-circuito, os seguintes são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="9313c-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a and b;
let x = And(a, b);
```