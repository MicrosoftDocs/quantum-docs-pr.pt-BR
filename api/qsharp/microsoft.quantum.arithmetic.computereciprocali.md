---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Operação ComputeReciprocalI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: 9024da4a457265c65a41ef681cfbb99ebd4989a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223350"
---
# <a name="computereciprocali-operation"></a><span data-ttu-id="49253-102">Operação ComputeReciprocalI</span><span class="sxs-lookup"><span data-stu-id="49253-102">ComputeReciprocalI operation</span></span>

<span data-ttu-id="49253-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="49253-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="49253-104">Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="49253-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="49253-105">Computa o 1/x recíproco para um inteiro sem sinal x usando divisão de inteiro.</span><span class="sxs-lookup"><span data-stu-id="49253-105">Computes the reciprocal 1/x for an unsigned integer x using integer division.</span></span> <span data-ttu-id="49253-106">O resultado, interpretado como um inteiro, será `floor(2^(2*n-1) / x)` .</span><span class="sxs-lookup"><span data-stu-id="49253-106">The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.</span></span>

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="49253-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="49253-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="49253-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="49253-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="49253-109">inteiro sem sinal de n bits</span><span class="sxs-lookup"><span data-stu-id="49253-109">n-bit unsigned integer</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="49253-110">resultado: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="49253-110">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="49253-111">2n-bit output, deve estar em $ \ket {0} $ inicialmente.</span><span class="sxs-lookup"><span data-stu-id="49253-111">2n-bit output, must be in $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="49253-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="49253-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="49253-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="49253-113">Remarks</span></span>

<span data-ttu-id="49253-114">Para a entrada x = 0, a saída será All-The.</span><span class="sxs-lookup"><span data-stu-id="49253-114">For the input x=0, the output will be all-ones.</span></span>