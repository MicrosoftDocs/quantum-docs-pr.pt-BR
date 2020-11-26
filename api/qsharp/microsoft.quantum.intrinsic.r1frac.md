---
uid: Microsoft.Quantum.Intrinsic.R1Frac
title: Operação R1Frac
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1Frac
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.

  \begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}). \end{align}

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r", and does not include the > factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".
ms.openlocfilehash: eb2dd8750ed5ad9fc75ca24bb4c8ef36298f69f4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198768"
---
# <a name="r1frac-operation"></a><span data-ttu-id="097a3-102">Operação R1Frac</span><span class="sxs-lookup"><span data-stu-id="097a3-102">R1Frac operation</span></span>

<span data-ttu-id="097a3-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="097a3-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="097a3-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="097a3-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="097a3-105">Aplica uma rotação sobre o estado $ \ket {1} $ por um ângulo especificado como uma fração dyadic.</span><span class="sxs-lookup"><span data-stu-id="097a3-105">Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="097a3-106">\begin{align} R_1 (n, k) \mathrel{: =} \operatorname{diag} (1, e ^ {i \pi k/2 ^ n}).</span><span class="sxs-lookup"><span data-stu-id="097a3-106">\begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}).</span></span>
<span data-ttu-id="097a3-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="097a3-107">\end{align}</span></span>

> [!WARNING]
> <span data-ttu-id="097a3-108">Esta operação usa a Convenção de sinal **oposta** de @"microsoft.quantum.intrinsic.r" e não inclui o fator de $1/2 $ incluído por @"microsoft.quantum.intrinsic.r1" .</span><span class="sxs-lookup"><span data-stu-id="097a3-108">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r", and does not include the factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".</span></span>

```qsharp
operation R1Frac (numerator : Int, power : Int, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="097a3-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="097a3-109">Input</span></span>

### <a name="numerator--int"></a><span data-ttu-id="097a3-110">numerador: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="097a3-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="097a3-111">O numerador na representação de fração dyadic do ângulo pelo qual o qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="097a3-111">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="097a3-112">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="097a3-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="097a3-113">Potência de dois especificando o denominador do ângulo pelo qual o qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="097a3-113">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="097a3-114">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="097a3-114">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="097a3-115">Qubit ao qual a portão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="097a3-115">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="097a3-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="097a3-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="097a3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="097a3-117">Remarks</span></span>

<span data-ttu-id="097a3-118">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="097a3-118">Equivalent to:</span></span>

```qsharp
RFrac(PauliZ, -numerator, denominator + 1, qubit);
RFrac(PauliI, numerator, denominator + 1, qubit);
```