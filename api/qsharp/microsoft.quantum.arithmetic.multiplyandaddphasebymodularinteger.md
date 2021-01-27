---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Operação MultiplyAndAddPhaseByModularInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: b1214acc2cafc3fede9fcb6663a435c0b1d2cf4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843073"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a><span data-ttu-id="8fa96-102">Operação MultiplyAndAddPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="8fa96-102">MultiplyAndAddPhaseByModularInteger operation</span></span>

<span data-ttu-id="8fa96-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8fa96-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8fa96-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8fa96-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8fa96-105">O mesmo que MultiplyAndAddByModularInteger, mas pressupõe que o soma codifica inteiros na base de QFT.</span><span class="sxs-lookup"><span data-stu-id="8fa96-105">The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.</span></span>

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="8fa96-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fa96-106">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="8fa96-107">constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8fa96-107">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8fa96-108">Um inteiro $a $ a ser adicionado a cada rótulo de estado base.</span><span class="sxs-lookup"><span data-stu-id="8fa96-108">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="8fa96-109">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8fa96-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8fa96-110">O módulo $N $ que adição e multiplicação são tomadas em relação a.</span><span class="sxs-lookup"><span data-stu-id="8fa96-110">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="8fa96-111">multiplicador: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8fa96-111">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8fa96-112">Um registro Quantum que representa um inteiro sem sinal cujo valor deve ser adicionado a cada rótulo de estado base de `summand` .</span><span class="sxs-lookup"><span data-stu-id="8fa96-112">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="phasesummand--phaselittleendian"></a><span data-ttu-id="8fa96-113">phaseSummand: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8fa96-113">phaseSummand : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="8fa96-114">Um registro Quantum que representa um inteiro não assinado para usar como o destino para esta operação.</span><span class="sxs-lookup"><span data-stu-id="8fa96-114">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8fa96-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8fa96-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8fa96-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fa96-116">Remarks</span></span>

<span data-ttu-id="8fa96-117">Pressupõe que `phaseSummand` tem o bit mais alto definido como 0.</span><span class="sxs-lookup"><span data-stu-id="8fa96-117">Assumes that `phaseSummand` has the highest bit set to 0.</span></span>
<span data-ttu-id="8fa96-118">Também pressupõe que o valor de `phaseSummand` é menor que $N $.</span><span class="sxs-lookup"><span data-stu-id="8fa96-118">Also assumes that the value of `phaseSummand` is less than $N$.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fa96-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8fa96-119">See Also</span></span>

- [<span data-ttu-id="8fa96-120">Microsoft. Quantum. aritmético. MultiplyAndAddByModularInteger</span><span class="sxs-lookup"><span data-stu-id="8fa96-120">Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)