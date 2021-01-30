---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Operação MultiplyByModularInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: bd4e0ad6c5bad779d9a31139690021fd9fcda210
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846504"
---
# <a name="multiplybymodularinteger-operation"></a><span data-ttu-id="a0d87-102">Operação MultiplyByModularInteger</span><span class="sxs-lookup"><span data-stu-id="a0d87-102">MultiplyByModularInteger operation</span></span>

<span data-ttu-id="a0d87-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a0d87-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a0d87-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a0d87-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a0d87-105">Executa a multiplicação modular por uma constante de inteiro em um registro de qubit.</span><span class="sxs-lookup"><span data-stu-id="a0d87-105">Performs modular multiplication by an integer constant on a qubit register.</span></span>

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a0d87-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0d87-106">Description</span></span>

<span data-ttu-id="a0d87-107">Vamos indicar `modulus` por $N $ e `constMultiplier` $a $.</span><span class="sxs-lookup"><span data-stu-id="a0d87-107">Let us denote `modulus` by $N$ and `constMultiplier` by $a$.</span></span>
<span data-ttu-id="a0d87-108">Em seguida, essa operação implementa uma operação unitário definida pelo seguinte mapa na base computacional: $ $ \begin{align} \ket{y} \mapsto \ket{(\cdot y) \operatorname{mod} N} \end{align} $ $ para todos os $y $ entre $0 $ e $N-$1.</span><span class="sxs-lookup"><span data-stu-id="a0d87-108">Then this operation implements a unitary operation defined by the following map on the computational basis: $$ \begin{align} \ket{y} \mapsto \ket{(a \cdot y) \operatorname{mod} N} \end{align} $$ for all $y$ between $0$ and $N - 1$.</span></span>

## <a name="input"></a><span data-ttu-id="a0d87-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0d87-109">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="a0d87-110">constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a0d87-110">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a0d87-111">Constante pela qual multiplicador está sendo multiplicado.</span><span class="sxs-lookup"><span data-stu-id="a0d87-111">Constant by which multiplier is being multiplied.</span></span> <span data-ttu-id="a0d87-112">Deve ser coprimo para o módulo.</span><span class="sxs-lookup"><span data-stu-id="a0d87-112">Must be co-prime to modulus.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="a0d87-113">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a0d87-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a0d87-114">A operação de multiplicação é executada no módulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="a0d87-114">The multiplication operation is performed modulo `modulus`.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="a0d87-115">multiplicador: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a0d87-115">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a0d87-116">O número que está sendo multiplicado por uma constante.</span><span class="sxs-lookup"><span data-stu-id="a0d87-116">The number being multiplied by a constant.</span></span>
<span data-ttu-id="a0d87-117">Esta é uma matriz de codificação qubits de um inteiro no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="a0d87-117">This is an array of qubits encoding an integer in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a0d87-118">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a0d87-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a0d87-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0d87-119">Remarks</span></span>

- <span data-ttu-id="a0d87-120">Para o diagrama de circuito e a explicação, consulte a Figura 7 na [página 8 de arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)</span><span class="sxs-lookup"><span data-stu-id="a0d87-120">For the circuit diagram and explanation see Figure 7 on [Page 8 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)</span></span>
- <span data-ttu-id="a0d87-121">Esta operação corresponde a U ₐ em [arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span><span class="sxs-lookup"><span data-stu-id="a0d87-121">This operation corresponds to Uₐ in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>