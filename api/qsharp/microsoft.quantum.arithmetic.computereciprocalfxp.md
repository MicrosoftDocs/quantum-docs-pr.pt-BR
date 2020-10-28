---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalFxP
title: Operação ComputeReciprocalFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalFxP
qsharp.summary: Computes $1/x$ for a fixed-point number $x$.
ms.openlocfilehash: e8f31d82fc69a3d7f4b571c4a679255dffc28b7f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694806"
---
# <a name="computereciprocalfxp-operation"></a><span data-ttu-id="ce4ef-102">Operação ComputeReciprocalFxP</span><span class="sxs-lookup"><span data-stu-id="ce4ef-102">ComputeReciprocalFxP operation</span></span>

<span data-ttu-id="ce4ef-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ce4ef-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ce4ef-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ce4ef-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ce4ef-105">Computa $1/x $ para um número de ponto fixo $x $.</span><span class="sxs-lookup"><span data-stu-id="ce4ef-105">Computes $1/x$ for a fixed-point number $x$.</span></span>

```qsharp
operation ComputeReciprocalFxP (x : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="ce4ef-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce4ef-106">Input</span></span>

### <a name="x--fixedpoint"></a><span data-ttu-id="ce4ef-107">x: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="ce4ef-107">x : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="ce4ef-108">Número de ponto fixo a ser invertido.</span><span class="sxs-lookup"><span data-stu-id="ce4ef-108">Fixed-point number to be inverted.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="ce4ef-109">resultado: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="ce4ef-109">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="ce4ef-110">Número de ponto fixo que manterá o resultado.</span><span class="sxs-lookup"><span data-stu-id="ce4ef-110">Fixed-point number that will hold the result.</span></span> <span data-ttu-id="ce4ef-111">Deve ser inicializado para $ \ket{0.0} $.</span><span class="sxs-lookup"><span data-stu-id="ce4ef-111">Must be initialized to $\ket{0.0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ce4ef-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ce4ef-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

