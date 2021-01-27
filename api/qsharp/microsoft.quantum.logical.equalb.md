---
uid: Microsoft.Quantum.Logical.EqualB
title: Função EqualB
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 2a15a749f52fe814db4fa57118f69c80fa22158a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817264"
---
# <a name="equalb-function"></a><span data-ttu-id="e7c01-102">Função EqualB</span><span class="sxs-lookup"><span data-stu-id="e7c01-102">EqualB function</span></span>

<span data-ttu-id="e7c01-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="e7c01-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="e7c01-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e7c01-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e7c01-105">Retorna true se e somente se duas entradas forem iguais.</span><span class="sxs-lookup"><span data-stu-id="e7c01-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="e7c01-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7c01-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="e7c01-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e7c01-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e7c01-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="e7c01-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="e7c01-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e7c01-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e7c01-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="e7c01-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e7c01-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e7c01-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e7c01-112">`true` se e somente se `a` for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="e7c01-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7c01-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7c01-113">Remarks</span></span>

<span data-ttu-id="e7c01-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="e7c01-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualB(a, b);
```