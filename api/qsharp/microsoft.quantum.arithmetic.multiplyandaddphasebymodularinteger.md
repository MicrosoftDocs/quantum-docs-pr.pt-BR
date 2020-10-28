---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Operação MultiplyAndAddPhaseByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: be7df50f040697329c2fe8bbc319c8cebb8b2687
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694565"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a><span data-ttu-id="c96c2-102">Operação MultiplyAndAddPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="c96c2-102">MultiplyAndAddPhaseByModularInteger operation</span></span>

<span data-ttu-id="c96c2-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c96c2-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c96c2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c96c2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c96c2-105">O mesmo que MultiplyAndAddByModularInteger, mas pressupõe que o soma codifica inteiros na base de QFT.</span><span class="sxs-lookup"><span data-stu-id="c96c2-105">The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.</span></span>

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="c96c2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c96c2-106">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="c96c2-107">constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c96c2-107">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c96c2-108">Um inteiro $a $ a ser adicionado a cada rótulo de estado base.</span><span class="sxs-lookup"><span data-stu-id="c96c2-108">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="c96c2-109">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c96c2-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c96c2-110">O módulo $N $ que adição e multiplicação são tomadas em relação a.</span><span class="sxs-lookup"><span data-stu-id="c96c2-110">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="c96c2-111">multiplicador: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c96c2-111">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c96c2-112">Um registro Quantum que representa um inteiro sem sinal cujo valor deve ser adicionado a cada rótulo de estado base de `summand` .</span><span class="sxs-lookup"><span data-stu-id="c96c2-112">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="phasesummand--phaselittleendian"></a><span data-ttu-id="c96c2-113">phaseSummand: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c96c2-113">phaseSummand : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="c96c2-114">Um registro Quantum que representa um inteiro não assinado para usar como o destino para esta operação.</span><span class="sxs-lookup"><span data-stu-id="c96c2-114">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c96c2-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c96c2-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c96c2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c96c2-116">Remarks</span></span>

<span data-ttu-id="c96c2-117">Pressupõe que `phaseSummand` tem o bit mais alto definido como 0.</span><span class="sxs-lookup"><span data-stu-id="c96c2-117">Assumes that `phaseSummand` has the highest bit set to 0.</span></span>
<span data-ttu-id="c96c2-118">Também pressupõe que o valor de `phaseSummand` é menor que $N $.</span><span class="sxs-lookup"><span data-stu-id="c96c2-118">Also assumes that the value of `phaseSummand` is less than $N$.</span></span>

## <a name="see-also"></a><span data-ttu-id="c96c2-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c96c2-119">See Also</span></span>

- [<span data-ttu-id="c96c2-120">Microsoft. Quantum. aritmético. MultiplyAndAddByModularInteger</span><span class="sxs-lookup"><span data-stu-id="c96c2-120">Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)