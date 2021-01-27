---
uid: Microsoft.Quantum.Logical.EqualL
title: Função de igual
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 58086f40ea20b6f1a5fa6996e3a6703e2bf66306
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815985"
---
# <a name="equall-function"></a><span data-ttu-id="a387f-102">Função de igual</span><span class="sxs-lookup"><span data-stu-id="a387f-102">EqualL function</span></span>

<span data-ttu-id="a387f-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a387f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a387f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a387f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a387f-105">Retorna true se e somente se duas entradas forem iguais.</span><span class="sxs-lookup"><span data-stu-id="a387f-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="a387f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a387f-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="a387f-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a387f-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a387f-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="a387f-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="a387f-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a387f-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a387f-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="a387f-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a387f-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a387f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a387f-112">`true` se e somente se `a` for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="a387f-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a387f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a387f-113">Remarks</span></span>

<span data-ttu-id="a387f-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="a387f-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualL(a, b);
```