---
uid: Microsoft.Quantum.Logical.EqualI
title: Função equali
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 6b805e76217e033cb0135cf85bd8f37a3eb8636a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693134"
---
# <a name="equali-function"></a><span data-ttu-id="42e41-102">Função equali</span><span class="sxs-lookup"><span data-stu-id="42e41-102">EqualI function</span></span>

<span data-ttu-id="42e41-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="42e41-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="42e41-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="42e41-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="42e41-105">Retorna true se e somente se duas entradas forem iguais.</span><span class="sxs-lookup"><span data-stu-id="42e41-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="42e41-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="42e41-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="42e41-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="42e41-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="42e41-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="42e41-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="42e41-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="42e41-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="42e41-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="42e41-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="42e41-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="42e41-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="42e41-112">`true` se e somente se `a` for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="42e41-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="42e41-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="42e41-113">Remarks</span></span>

<span data-ttu-id="42e41-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="42e41-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualI(a, b);
```