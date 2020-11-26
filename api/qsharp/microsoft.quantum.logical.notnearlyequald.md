---
uid: Microsoft.Quantum.Logical.NotNearlyEqualD
title: Função NotNearlyEqualD
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotNearlyEqualD
qsharp.summary: Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).
ms.openlocfilehash: 23229b1630982eba4485330cc2290aed733c4d86
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197136"
---
# <a name="notnearlyequald-function"></a><span data-ttu-id="79278-102">Função NotNearlyEqualD</span><span class="sxs-lookup"><span data-stu-id="79278-102">NotNearlyEqualD function</span></span>

<span data-ttu-id="79278-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="79278-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="79278-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="79278-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="79278-105">Retorna true se e somente se duas entradas não forem quase iguais (ou seja, não estiverem dentro de uma tolerância de 1e-12).</span><span class="sxs-lookup"><span data-stu-id="79278-105">Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).</span></span>

```qsharp
function NotNearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="79278-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="79278-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="79278-107">r: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="79278-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="79278-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="79278-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="79278-109">b: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="79278-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="79278-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="79278-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="79278-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="79278-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="79278-112">`true` se e somente se `a` não for quase igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="79278-112">`true` if and only if `a` is not nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="79278-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="79278-113">Remarks</span></span>

<span data-ttu-id="79278-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="79278-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) >= 1e-12;
let cond = NotNearlyEqualD(a, b);
```