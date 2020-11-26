---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: Operação IncrementPhaseByModularInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 6a39ce49dfa28c1f1cbe6b29e526144c3ac19e53
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222874"
---
# <a name="incrementphasebymodularinteger-operation"></a><span data-ttu-id="e7c18-102">Operação IncrementPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="e7c18-102">IncrementPhaseByModularInteger operation</span></span>

<span data-ttu-id="e7c18-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e7c18-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e7c18-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e7c18-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e7c18-105">Executa um incremento modular de um registro qubit por uma constante de inteiro.</span><span class="sxs-lookup"><span data-stu-id="e7c18-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="e7c18-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7c18-106">Description</span></span>

<span data-ttu-id="e7c18-107">Vamos indicar `increment` por $a $, `modulus` por $N $ e inteiro codificado `target` por $y $.</span><span class="sxs-lookup"><span data-stu-id="e7c18-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="e7c18-108">Em seguida, a operação executa a seguinte transformação: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} inteiros são codificados no formato little-endian na base QFT.</span><span class="sxs-lookup"><span data-stu-id="e7c18-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format in QFT basis.</span></span>

## <a name="input"></a><span data-ttu-id="e7c18-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7c18-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="e7c18-110">incremento: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e7c18-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e7c18-111">Incremento inteiro $a $ a ser adicionado a $y $.</span><span class="sxs-lookup"><span data-stu-id="e7c18-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="e7c18-112">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e7c18-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e7c18-113">Integer $N $ que mods $y + a $.</span><span class="sxs-lookup"><span data-stu-id="e7c18-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="e7c18-114">destino: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e7c18-114">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="e7c18-115">Integer $y $ no formato little-endian codificado em fases que `increment` $a $ é adicionado a.</span><span class="sxs-lookup"><span data-stu-id="e7c18-115">Integer $y$ in phase-encoded little-endian format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e7c18-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e7c18-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e7c18-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7c18-117">Remarks</span></span>

<span data-ttu-id="e7c18-118">Pressupõe que `target` tem o bit mais alto definido como 0.</span><span class="sxs-lookup"><span data-stu-id="e7c18-118">Assumes that `target` has the highest bit set to 0.</span></span>
<span data-ttu-id="e7c18-119">Também pressupõe que o valor de destino seja menor que $N $.</span><span class="sxs-lookup"><span data-stu-id="e7c18-119">Also assumes that the value of target is less than $N$.</span></span>

<span data-ttu-id="e7c18-120">Para o diagrama de circuito e a explicação, consulte a Figura 5 na [página 5 de arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).</span><span class="sxs-lookup"><span data-stu-id="e7c18-120">For the circuit diagram and explanation see Figure 5 on [Page 5 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).</span></span>

## <a name="see-also"></a><span data-ttu-id="e7c18-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e7c18-121">See Also</span></span>

- [<span data-ttu-id="e7c18-122">Microsoft. Quantum. aritmético. IncrementByModularInteger</span><span class="sxs-lookup"><span data-stu-id="e7c18-122">Microsoft.Quantum.Arithmetic.IncrementByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByModularInteger)