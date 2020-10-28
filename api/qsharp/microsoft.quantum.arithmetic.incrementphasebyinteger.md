---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: Operação IncrementPhaseByInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fb67455dadbc7a2f38880581f0e413a747faa8ef
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694777"
---
# <a name="incrementphasebyinteger-operation"></a><span data-ttu-id="f6b10-102">Operação IncrementPhaseByInteger</span><span class="sxs-lookup"><span data-stu-id="f6b10-102">IncrementPhaseByInteger operation</span></span>

<span data-ttu-id="f6b10-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f6b10-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f6b10-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f6b10-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f6b10-105">Incrementa um registro de Quantum não assinado por um inteiro clássico, usando rotações de fase.</span><span class="sxs-lookup"><span data-stu-id="f6b10-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="f6b10-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6b10-106">Description</span></span>

<span data-ttu-id="f6b10-107">Suponha que `target` o codifica um inteiro sem sinal $x $ em uma codificação little-endian e que `increment` seja igual a $a $.</span><span class="sxs-lookup"><span data-stu-id="f6b10-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="f6b10-108">Em seguida, essa operação implementa o unitário $ \ket{x} \mapsto \ket{x + a} $, em que a adição é executada módulo $2 ^ n $, em que $n = \texttt{Length (Target!)} $.</span><span class="sxs-lookup"><span data-stu-id="f6b10-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="f6b10-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f6b10-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="f6b10-110">incremento: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f6b10-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f6b10-111">O inteiro pelo qual o `target` é incrementado por.</span><span class="sxs-lookup"><span data-stu-id="f6b10-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="f6b10-112">destino: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f6b10-112">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="f6b10-113">Um Quantum registra a codificação de um inteiro não assinado usando a codificação little-endian na base dupla (QFT).</span><span class="sxs-lookup"><span data-stu-id="f6b10-113">A quantum register encoding an unsigned integer using little-endian encoding in the dual (QFT) basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f6b10-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f6b10-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f6b10-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6b10-115">Remarks</span></span>

<span data-ttu-id="f6b10-116">Observe que simplificamos o circuito porque o incremento é uma constante clássica, não um registro do Quantum.</span><span class="sxs-lookup"><span data-stu-id="f6b10-116">Note that we have simplified the circuit because the increment is a classical constant, not a quantum register.</span></span>

<span data-ttu-id="f6b10-117">Veja a figura na [ página 6 de arXiv: Quant-pH/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) para o diagrama e a explicação do circuito.</span><span class="sxs-lookup"><span data-stu-id="f6b10-117">See the figure on [ Page 6 of arXiv:quant-ph/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) for the circuit diagram and explanation.</span></span>

## <a name="references"></a><span data-ttu-id="f6b10-118">Referências</span><span class="sxs-lookup"><span data-stu-id="f6b10-118">References</span></span>

- [<span data-ttu-id="f6b10-119">*Thomas G. Draper* , arXiv: Quant-pH/0008033</span><span class="sxs-lookup"><span data-stu-id="f6b10-119"> *Thomas G. Draper* , arXiv:quant-ph/0008033</span></span>](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a><span data-ttu-id="f6b10-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f6b10-120">See Also</span></span>

- [<span data-ttu-id="f6b10-121">Microsoft. Quantum. aritmético. IncrementByInteger</span><span class="sxs-lookup"><span data-stu-id="f6b10-121">Microsoft.Quantum.Arithmetic.IncrementByInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)