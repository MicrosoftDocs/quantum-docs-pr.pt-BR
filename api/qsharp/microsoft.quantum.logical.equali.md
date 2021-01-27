---
uid: Microsoft.Quantum.Logical.EqualI
title: Função equali
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 87cf00ea8bb738cda30092b3d80940291beb1fb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98816744"
---
# <a name="equali-function"></a><span data-ttu-id="25be4-102">Função equali</span><span class="sxs-lookup"><span data-stu-id="25be4-102">EqualI function</span></span>

<span data-ttu-id="25be4-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="25be4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="25be4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25be4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25be4-105">Retorna true se e somente se duas entradas forem iguais.</span><span class="sxs-lookup"><span data-stu-id="25be4-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="25be4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="25be4-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="25be4-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="25be4-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="25be4-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="25be4-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="25be4-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="25be4-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="25be4-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="25be4-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="25be4-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="25be4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="25be4-112">`true` se e somente se `a` for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="25be4-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="25be4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="25be4-113">Remarks</span></span>

<span data-ttu-id="25be4-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="25be4-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualI(a, b);
```