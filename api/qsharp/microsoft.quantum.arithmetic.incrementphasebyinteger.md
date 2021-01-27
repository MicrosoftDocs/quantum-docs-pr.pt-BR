---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: Operação IncrementPhaseByInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: cc7922b2940cb979394958d5eb4e9933144eb062
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843156"
---
# <a name="incrementphasebyinteger-operation"></a><span data-ttu-id="f5ec1-102">Operação IncrementPhaseByInteger</span><span class="sxs-lookup"><span data-stu-id="f5ec1-102">IncrementPhaseByInteger operation</span></span>

<span data-ttu-id="f5ec1-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f5ec1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f5ec1-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f5ec1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f5ec1-105">Incrementa um registro de Quantum não assinado por um inteiro clássico, usando rotações de fase.</span><span class="sxs-lookup"><span data-stu-id="f5ec1-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="f5ec1-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5ec1-106">Description</span></span>

<span data-ttu-id="f5ec1-107">Suponha que `target` o codifica um inteiro sem sinal $x $ em uma codificação little-endian e que `increment` seja igual a $a $.</span><span class="sxs-lookup"><span data-stu-id="f5ec1-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="f5ec1-108">Em seguida, essa operação implementa o unitário $ \ket{x} \mapsto \ket{x + a} $, em que a adição é executada módulo $2 ^ n $, em que $n = \texttt{Length (Target!)} $.</span><span class="sxs-lookup"><span data-stu-id="f5ec1-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="f5ec1-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5ec1-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="f5ec1-110">incremento: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f5ec1-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f5ec1-111">O inteiro pelo qual o `target` é incrementado por.</span><span class="sxs-lookup"><span data-stu-id="f5ec1-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="f5ec1-112">destino: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f5ec1-112">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="f5ec1-113">Um Quantum registra a codificação de um inteiro não assinado usando a codificação little-endian na base dupla (QFT).</span><span class="sxs-lookup"><span data-stu-id="f5ec1-113">A quantum register encoding an unsigned integer using little-endian encoding in the dual (QFT) basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f5ec1-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f5ec1-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f5ec1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5ec1-115">Remarks</span></span>

<span data-ttu-id="f5ec1-116">Observe que simplificamos o circuito porque o incremento é uma constante clássica, não um registro do Quantum.</span><span class="sxs-lookup"><span data-stu-id="f5ec1-116">Note that we have simplified the circuit because the increment is a classical constant, not a quantum register.</span></span>

<span data-ttu-id="f5ec1-117">Veja a figura na [ página 6 de arXiv: Quant-pH/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) para o diagrama e a explicação do circuito.</span><span class="sxs-lookup"><span data-stu-id="f5ec1-117">See the figure on [ Page 6 of arXiv:quant-ph/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) for the circuit diagram and explanation.</span></span>

## <a name="references"></a><span data-ttu-id="f5ec1-118">Referências</span><span class="sxs-lookup"><span data-stu-id="f5ec1-118">References</span></span>

- [<span data-ttu-id="f5ec1-119">*Thomas G. Draper*, arXiv: Quant-pH/0008033</span><span class="sxs-lookup"><span data-stu-id="f5ec1-119"> *Thomas G. Draper*, arXiv:quant-ph/0008033</span></span>](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a><span data-ttu-id="f5ec1-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f5ec1-120">See Also</span></span>

- [<span data-ttu-id="f5ec1-121">Microsoft. Quantum. aritmético. IncrementByInteger</span><span class="sxs-lookup"><span data-stu-id="f5ec1-121">Microsoft.Quantum.Arithmetic.IncrementByInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)