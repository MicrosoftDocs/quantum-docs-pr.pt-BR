---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Função IntegerBits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: ab459cd841cdac116cf0e98c094834f628b6a2d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694572"
---
# <a name="integerbits-function"></a><span data-ttu-id="34dd6-102">Função IntegerBits</span><span class="sxs-lookup"><span data-stu-id="34dd6-102">IntegerBits function</span></span>

<span data-ttu-id="34dd6-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="34dd6-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="34dd6-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="34dd6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="34dd6-105">Retorna todas as posições nas quais os bits de um inteiro são definidos.</span><span class="sxs-lookup"><span data-stu-id="34dd6-105">Returns all positions in which bits of an integer are set.</span></span>

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="34dd6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="34dd6-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="34dd6-107">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="34dd6-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="34dd6-108">Um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="34dd6-108">A nonnegative number.</span></span>


### <a name="length--int"></a><span data-ttu-id="34dd6-109">comprimento: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="34dd6-109">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="34dd6-110">O número de bits na expansão binária de `value` .</span><span class="sxs-lookup"><span data-stu-id="34dd6-110">The number of bits in the binary expansion of `value`.</span></span>



## <a name="output--int"></a><span data-ttu-id="34dd6-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="34dd6-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="34dd6-112">Uma matriz que contém todas as posições de bits (a partir de 0) que são 1 na expansão binária, `value` Considerando todos os bits até a posição `length - 1` .</span><span class="sxs-lookup"><span data-stu-id="34dd6-112">An array containing all bit positions (starting from 0) that are 1 in the binary expansion of `value` considering all bits up to position `length - 1`.</span></span>  <span data-ttu-id="34dd6-113">Todas as posições são ordenadas na matriz por posição em uma ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="34dd6-113">All positions are ordered in the array by position in an increasing order.</span></span>