---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Função LeftShiftedI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: ce68311adf211169c2fb499bb189332370a6d6ac
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694375"
---
# <a name="leftshiftedi-function"></a><span data-ttu-id="00361-102">Função LeftShiftedI</span><span class="sxs-lookup"><span data-stu-id="00361-102">LeftShiftedI function</span></span>

<span data-ttu-id="00361-103">Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="00361-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="00361-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="00361-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="00361-105">Desloca a representação bit a bit de um número à esquerda por um determinado número de bits.</span><span class="sxs-lookup"><span data-stu-id="00361-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="00361-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="00361-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="00361-107">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="00361-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="00361-108">O número cuja representação em bits bit a lado deve ser deslocada para a esquerda (mais significativa).</span><span class="sxs-lookup"><span data-stu-id="00361-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="00361-109">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="00361-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="00361-110">O número de bits pelo qual deve `value` ser deslocado para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="00361-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--int"></a><span data-ttu-id="00361-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="00361-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="00361-112">O valor de `value` , deslocado para a esquerda por `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="00361-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="00361-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="00361-113">Remarks</span></span>

<span data-ttu-id="00361-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="00361-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```