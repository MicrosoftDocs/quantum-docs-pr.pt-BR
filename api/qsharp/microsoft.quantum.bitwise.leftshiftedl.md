---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: Função LeftShiftedL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 17e5c845755f74e9703381bc82bfd63be836d038
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694370"
---
# <a name="leftshiftedl-function"></a><span data-ttu-id="7a7d2-102">Função LeftShiftedL</span><span class="sxs-lookup"><span data-stu-id="7a7d2-102">LeftShiftedL function</span></span>

<span data-ttu-id="7a7d2-103">Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="7a7d2-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="7a7d2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7a7d2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7a7d2-105">Desloca a representação bit a bit de um número à esquerda por um determinado número de bits.</span><span class="sxs-lookup"><span data-stu-id="7a7d2-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="7a7d2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7a7d2-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="7a7d2-107">valor: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="7a7d2-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="7a7d2-108">O número cuja representação em bits bit a lado deve ser deslocada para a esquerda (mais significativa).</span><span class="sxs-lookup"><span data-stu-id="7a7d2-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="7a7d2-109">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7a7d2-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7a7d2-110">O número de bits pelo qual deve `value` ser deslocado para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="7a7d2-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="7a7d2-111">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="7a7d2-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="7a7d2-112">O valor de `value` , deslocado para a esquerda por `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="7a7d2-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a7d2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a7d2-113">Remarks</span></span>

<span data-ttu-id="7a7d2-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="7a7d2-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedL(a, b);
```