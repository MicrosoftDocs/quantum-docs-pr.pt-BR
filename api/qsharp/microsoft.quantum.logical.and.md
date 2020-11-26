---
uid: Microsoft.Quantum.Logical.And
title: Função and
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 279221ed785dd76e28146e4c22e70290936bf529
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198564"
---
# <a name="and-function"></a><span data-ttu-id="2742b-102">Função and</span><span class="sxs-lookup"><span data-stu-id="2742b-102">And function</span></span>

<span data-ttu-id="2742b-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2742b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2742b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2742b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2742b-105">Retorna a conjunção booliana de dois valores.</span><span class="sxs-lookup"><span data-stu-id="2742b-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="2742b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2742b-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="2742b-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2742b-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2742b-108">O primeiro valor a ser considerado.</span><span class="sxs-lookup"><span data-stu-id="2742b-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="2742b-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2742b-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2742b-110">O segundo valor a ser considerado.</span><span class="sxs-lookup"><span data-stu-id="2742b-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2742b-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2742b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2742b-112">`true` se e somente se `a` e `b` forem ambos `true` .</span><span class="sxs-lookup"><span data-stu-id="2742b-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2742b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2742b-113">Remarks</span></span>

<span data-ttu-id="2742b-114">Ao contrário do `and` operador, essa função não é de curto circuito, de modo que ambas as entradas são totalmente avaliadas.</span><span class="sxs-lookup"><span data-stu-id="2742b-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="2742b-115">Até o comportamento de curto-circuito, os seguintes são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="2742b-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a and b;
let x = And(a, b);
```