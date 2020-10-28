---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: Operação MultiplyAndAddByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: 3f85f6aaea1d6f8095709c6f387322df7a5e047c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694566"
---
# <a name="multiplyandaddbymodularinteger-operation"></a><span data-ttu-id="57694-102">Operação MultiplyAndAddByModularInteger</span><span class="sxs-lookup"><span data-stu-id="57694-102">MultiplyAndAddByModularInteger operation</span></span>

<span data-ttu-id="57694-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="57694-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="57694-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="57694-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="57694-105">Executa uma multiplicação modular e adicionar por constantes de inteiro em um registro de qubit.</span><span class="sxs-lookup"><span data-stu-id="57694-105">Performs a modular multiply-and-add by integer constants on a qubit register.</span></span>

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="57694-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="57694-106">Description</span></span>

<span data-ttu-id="57694-107">Implementa o MAP $ $ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatorname{mod} N} \end{align} $ $ para um determinado módulo $N $, um multiplicador constante $a $ e soma $y $.</span><span class="sxs-lookup"><span data-stu-id="57694-107">Implements the map $$ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatorname{mod} N} \end{align} $$ for a given modulus $N$, constant multiplier $a$, and summand $y$.</span></span>

## <a name="input"></a><span data-ttu-id="57694-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="57694-108">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="57694-109">constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="57694-109">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="57694-110">Um inteiro $a $ a ser adicionado a cada rótulo de estado base.</span><span class="sxs-lookup"><span data-stu-id="57694-110">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="57694-111">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="57694-111">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="57694-112">O módulo $N $ que adição e multiplicação são tomadas em relação a.</span><span class="sxs-lookup"><span data-stu-id="57694-112">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="57694-113">multiplicador: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="57694-113">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="57694-114">Um registro Quantum que representa um inteiro sem sinal cujo valor deve ser adicionado a cada rótulo de estado base de `summand` .</span><span class="sxs-lookup"><span data-stu-id="57694-114">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="summand--littleendian"></a><span data-ttu-id="57694-115">soma: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="57694-115">summand : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="57694-116">Um registro Quantum que representa um inteiro não assinado para usar como o destino para esta operação.</span><span class="sxs-lookup"><span data-stu-id="57694-116">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="57694-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="57694-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="57694-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="57694-118">Remarks</span></span>

- <span data-ttu-id="57694-119">Para o diagrama de circuito e a explicação, consulte a Figura 6 na [página 7 de arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)</span><span class="sxs-lookup"><span data-stu-id="57694-119">For the circuit diagram and explanation see Figure 6 on [Page 7 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)</span></span>
- <span data-ttu-id="57694-120">Esta operação corresponde a CMULT (a) MOD (N) em [arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span><span class="sxs-lookup"><span data-stu-id="57694-120">This operation corresponds to CMULT(a)MOD(N) in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>

## <a name="see-also"></a><span data-ttu-id="57694-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="57694-121">See Also</span></span>

- [<span data-ttu-id="57694-122">Microsoft. Quantum. aritmético. MultiplyAndAddPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="57694-122">Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)