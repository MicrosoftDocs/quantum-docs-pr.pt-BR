---
uid: Microsoft.Quantum.Logical.NearlyEqualD
title: Função NearlyEqualD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NearlyEqualD
qsharp.summary: Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).
ms.openlocfilehash: 332f9ea1753b539eba7b931d5b948b2a238d1abf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693108"
---
# <a name="nearlyequald-function"></a><span data-ttu-id="2cdab-102">Função NearlyEqualD</span><span class="sxs-lookup"><span data-stu-id="2cdab-102">NearlyEqualD function</span></span>

<span data-ttu-id="2cdab-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2cdab-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2cdab-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2cdab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2cdab-105">Retorna true se e somente se duas entradas forem quase iguais (ou seja, dentro de uma tolerância de 1e-12).</span><span class="sxs-lookup"><span data-stu-id="2cdab-105">Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).</span></span>

```qsharp
function NearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="2cdab-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2cdab-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="2cdab-107">r: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2cdab-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2cdab-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="2cdab-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="2cdab-109">b: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2cdab-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2cdab-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="2cdab-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2cdab-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2cdab-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2cdab-112">`true` se e somente se `a` for quase igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="2cdab-112">`true` if and only if `a` is nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cdab-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cdab-113">Remarks</span></span>

<span data-ttu-id="2cdab-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="2cdab-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) < 1e-12;
let cond = NearlyEqualD(a, b);
```