---
uid: Microsoft.Quantum.Logical.NotEqualD
title: Função não igual a
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualD
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 4599d7125dbc67547af454183f620e8d84f2caf7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197238"
---
# <a name="notequald-function"></a><span data-ttu-id="7c4d3-102">Função não igual a</span><span class="sxs-lookup"><span data-stu-id="7c4d3-102">NotEqualD function</span></span>

<span data-ttu-id="7c4d3-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="7c4d3-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="7c4d3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7c4d3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7c4d3-105">Retorna true se e somente se duas entradas não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="7c4d3-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="7c4d3-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c4d3-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="7c4d3-107">r: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7c4d3-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7c4d3-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="7c4d3-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="7c4d3-109">b: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7c4d3-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7c4d3-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="7c4d3-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="7c4d3-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7c4d3-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7c4d3-112">`true` se e somente se `a` não for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="7c4d3-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c4d3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c4d3-113">Remarks</span></span>

<span data-ttu-id="7c4d3-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="7c4d3-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualD(a, b);
```