---
uid: Microsoft.Quantum.Intrinsic.R1Frac
title: Operação R1Frac
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1Frac
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.

  \begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}). \end{align}

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r", and does not include the > factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".
ms.openlocfilehash: bfa6cd60eebd05feec8cfa2bf71e09dc0d02843a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694748"
---
# <a name="r1frac-operation"></a><span data-ttu-id="d80c5-102">Operação R1Frac</span><span class="sxs-lookup"><span data-stu-id="d80c5-102">R1Frac operation</span></span>

<span data-ttu-id="d80c5-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="d80c5-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="d80c5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d80c5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d80c5-105">Aplica uma rotação sobre o estado $ \ket {1} $ por um ângulo especificado como uma fração dyadic.</span><span class="sxs-lookup"><span data-stu-id="d80c5-105">Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="d80c5-106">\begin{align} R_1 (n, k) \mathrel{: =} \operatorname{diag} (1, e ^ {i \pi k/2 ^ n}).</span><span class="sxs-lookup"><span data-stu-id="d80c5-106">\begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}).</span></span>
<span data-ttu-id="d80c5-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="d80c5-107">\end{align}</span></span>

> [!WARNING]
> <span data-ttu-id="d80c5-108">Esta operação usa a Convenção de sinal **oposta** de @"microsoft.quantum.intrinsic.r" e não inclui o fator de $1/2 $ incluído por @"microsoft.quantum.intrinsic.r1" .</span><span class="sxs-lookup"><span data-stu-id="d80c5-108">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r", and does not include the factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".</span></span>

```qsharp
operation R1Frac (numerator : Int, power : Int, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="d80c5-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="d80c5-109">Input</span></span>

### <a name="numerator--int"></a><span data-ttu-id="d80c5-110">numerador: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d80c5-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d80c5-111">O numerador na representação de fração dyadic do ângulo pelo qual o qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="d80c5-111">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="d80c5-112">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d80c5-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d80c5-113">Potência de dois especificando o denominador do ângulo pelo qual o qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="d80c5-113">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="d80c5-114">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d80c5-114">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d80c5-115">Qubit ao qual a portão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="d80c5-115">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d80c5-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d80c5-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d80c5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d80c5-117">Remarks</span></span>

<span data-ttu-id="d80c5-118">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="d80c5-118">Equivalent to:</span></span>

```qsharp
RFrac(PauliZ, -numerator, denominator + 1, qubit);
RFrac(PauliI, numerator, denominator + 1, qubit);
```