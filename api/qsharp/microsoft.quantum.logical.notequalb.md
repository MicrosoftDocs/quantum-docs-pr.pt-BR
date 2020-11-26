---
uid: Microsoft.Quantum.Logical.NotEqualB
title: Função NotEqualB
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 7943411b662683df058213a9e4b8eb7c9329ff07
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197374"
---
# <a name="notequalb-function"></a><span data-ttu-id="562e7-102">Função NotEqualB</span><span class="sxs-lookup"><span data-stu-id="562e7-102">NotEqualB function</span></span>

<span data-ttu-id="562e7-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="562e7-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="562e7-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="562e7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="562e7-105">Retorna true se e somente se duas entradas não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="562e7-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="562e7-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="562e7-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="562e7-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="562e7-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="562e7-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="562e7-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="562e7-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="562e7-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="562e7-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="562e7-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="562e7-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="562e7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="562e7-112">`true` se e somente se `a` não for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="562e7-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="562e7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="562e7-113">Remarks</span></span>

<span data-ttu-id="562e7-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="562e7-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualB(a, b);
```