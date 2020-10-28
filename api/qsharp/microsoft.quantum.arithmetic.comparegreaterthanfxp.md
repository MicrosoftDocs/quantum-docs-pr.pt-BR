---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Operação CompareGreaterThanFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: bd3bcedd7a4a81fc600f7f4b6bdf1d2a797abbd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694814"
---
# <a name="comparegreaterthanfxp-operation"></a><span data-ttu-id="62f3f-102">Operação CompareGreaterThanFxP</span><span class="sxs-lookup"><span data-stu-id="62f3f-102">CompareGreaterThanFxP operation</span></span>

<span data-ttu-id="62f3f-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="62f3f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="62f3f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="62f3f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="62f3f-105">Compara dois números de ponto fixo armazenados em registros de Quantum e controla uma inversão no resultado.</span><span class="sxs-lookup"><span data-stu-id="62f3f-105">Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.</span></span>

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="62f3f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="62f3f-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="62f3f-107">FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="62f3f-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="62f3f-108">Primeiro número de ponto fixo a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="62f3f-108">First fixed-point number to be compared.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="62f3f-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="62f3f-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="62f3f-110">Segundo número de ponto fixo a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="62f3f-110">Second fixed-point number to be compared.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="62f3f-111">resultado: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="62f3f-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="62f3f-112">Resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="62f3f-112">Result of the comparison.</span></span> <span data-ttu-id="62f3f-113">Será invertida se `fp1 > fp2` .</span><span class="sxs-lookup"><span data-stu-id="62f3f-113">Will be flipped if `fp1 > fp2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="62f3f-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="62f3f-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="62f3f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="62f3f-115">Remarks</span></span>

<span data-ttu-id="62f3f-116">A implementação atual requer que os dois números de ponto fixo tenham a mesma posição de ponto e o mesmo número de qubits.</span><span class="sxs-lookup"><span data-stu-id="62f3f-116">The current implementation requires the two fixed-point numbers to have the same point position and the same number of qubits.</span></span>