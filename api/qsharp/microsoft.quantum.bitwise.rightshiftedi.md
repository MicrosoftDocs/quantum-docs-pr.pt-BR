---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Função RightShiftedI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b0ca7d3cb84c58429e9b3a29893a6140a717006b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694361"
---
# <a name="rightshiftedi-function"></a><span data-ttu-id="46327-102">Função RightShiftedI</span><span class="sxs-lookup"><span data-stu-id="46327-102">RightShiftedI function</span></span>

<span data-ttu-id="46327-103">Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="46327-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="46327-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="46327-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="46327-105">Desloca a representação bit a bit de um número à direita por um determinado número de bits.</span><span class="sxs-lookup"><span data-stu-id="46327-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="46327-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="46327-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="46327-107">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="46327-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="46327-108">O número cuja representação em bits bit a lado deve ser deslocada para a direita (menos significativa).</span><span class="sxs-lookup"><span data-stu-id="46327-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="46327-109">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="46327-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="46327-110">O número de bits pelo qual deve `value` ser deslocado para a direita.</span><span class="sxs-lookup"><span data-stu-id="46327-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--int"></a><span data-ttu-id="46327-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="46327-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="46327-112">O valor de `value` , deslocado para a direita por `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="46327-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="46327-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="46327-113">Remarks</span></span>

<span data-ttu-id="46327-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="46327-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```