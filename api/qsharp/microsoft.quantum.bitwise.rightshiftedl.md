---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: Função RightShiftedL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 2929ba58b636847257391930e1019769fd2c2580
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694360"
---
# <a name="rightshiftedl-function"></a><span data-ttu-id="61f27-102">Função RightShiftedL</span><span class="sxs-lookup"><span data-stu-id="61f27-102">RightShiftedL function</span></span>

<span data-ttu-id="61f27-103">Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="61f27-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="61f27-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="61f27-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="61f27-105">Desloca a representação bit a bit de um número à direita por um determinado número de bits.</span><span class="sxs-lookup"><span data-stu-id="61f27-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="61f27-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="61f27-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="61f27-107">valor: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="61f27-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="61f27-108">O número cuja representação em bits bit a lado deve ser deslocada para a direita (menos significativa).</span><span class="sxs-lookup"><span data-stu-id="61f27-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="61f27-109">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="61f27-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="61f27-110">O número de bits pelo qual deve `value` ser deslocado para a direita.</span><span class="sxs-lookup"><span data-stu-id="61f27-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="61f27-111">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="61f27-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="61f27-112">O valor de `value` , deslocado para a direita por `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="61f27-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="61f27-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="61f27-113">Remarks</span></span>

<span data-ttu-id="61f27-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="61f27-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedL(a, b);
```