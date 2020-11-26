---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Função LeftShiftedI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 3a7220489bfa241e2337df14291bafb1d6e0e19e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209852"
---
# <a name="leftshiftedi-function"></a><span data-ttu-id="01a60-102">Função LeftShiftedI</span><span class="sxs-lookup"><span data-stu-id="01a60-102">LeftShiftedI function</span></span>

<span data-ttu-id="01a60-103">Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="01a60-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="01a60-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="01a60-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="01a60-105">Desloca a representação bit a bit de um número à esquerda por um determinado número de bits.</span><span class="sxs-lookup"><span data-stu-id="01a60-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="01a60-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="01a60-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="01a60-107">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01a60-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="01a60-108">O número cuja representação em bits bit a lado deve ser deslocada para a esquerda (mais significativa).</span><span class="sxs-lookup"><span data-stu-id="01a60-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="01a60-109">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01a60-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="01a60-110">O número de bits pelo qual deve `value` ser deslocado para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="01a60-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--int"></a><span data-ttu-id="01a60-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01a60-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="01a60-112">O valor de `value` , deslocado para a esquerda por `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="01a60-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="01a60-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="01a60-113">Remarks</span></span>

<span data-ttu-id="01a60-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="01a60-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```