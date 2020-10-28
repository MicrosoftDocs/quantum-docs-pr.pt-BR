---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Operação ComputeReciprocalI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: b99e816ed69af6e6d1758442d6f95c5ab0e5c07a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694802"
---
# <a name="computereciprocali-operation"></a><span data-ttu-id="d7409-102">Operação ComputeReciprocalI</span><span class="sxs-lookup"><span data-stu-id="d7409-102">ComputeReciprocalI operation</span></span>

<span data-ttu-id="d7409-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d7409-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d7409-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d7409-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d7409-105">Computa o 1/x recíproco para um inteiro sem sinal x usando divisão de inteiro.</span><span class="sxs-lookup"><span data-stu-id="d7409-105">Computes the reciprocal 1/x for an unsigned integer x using integer division.</span></span> <span data-ttu-id="d7409-106">O resultado, interpretado como um inteiro, será `floor(2^(2*n-1) / x)` .</span><span class="sxs-lookup"><span data-stu-id="d7409-106">The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.</span></span>

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="d7409-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7409-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="d7409-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d7409-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d7409-109">inteiro sem sinal de n bits</span><span class="sxs-lookup"><span data-stu-id="d7409-109">n-bit unsigned integer</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="d7409-110">resultado: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d7409-110">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d7409-111">2n-bit output, deve estar em $ \ket {0} $ inicialmente.</span><span class="sxs-lookup"><span data-stu-id="d7409-111">2n-bit output, must be in $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d7409-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d7409-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d7409-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7409-113">Remarks</span></span>

<span data-ttu-id="d7409-114">Para a entrada x = 0, a saída será All-The.</span><span class="sxs-lookup"><span data-stu-id="d7409-114">For the input x=0, the output will be all-ones.</span></span>