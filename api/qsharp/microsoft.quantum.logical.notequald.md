---
uid: Microsoft.Quantum.Logical.NotEqualD
title: Função não igual a
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualD
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: dd21fcc1d0d73bd210303bfbf4f336386b912107
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696805"
---
# <a name="notequald-function"></a><span data-ttu-id="53822-102">Função não igual a</span><span class="sxs-lookup"><span data-stu-id="53822-102">NotEqualD function</span></span>

<span data-ttu-id="53822-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="53822-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="53822-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="53822-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="53822-105">Retorna true se e somente se duas entradas não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="53822-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="53822-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="53822-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="53822-107">r: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="53822-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="53822-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="53822-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="53822-109">b: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="53822-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="53822-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="53822-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="53822-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="53822-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="53822-112">`true` se e somente se `a` não for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="53822-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="53822-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="53822-113">Remarks</span></span>

<span data-ttu-id="53822-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="53822-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualD(a, b);
```