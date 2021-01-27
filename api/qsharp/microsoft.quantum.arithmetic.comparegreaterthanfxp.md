---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Operação CompareGreaterThanFxP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: f49c713c8a1e8a6451f2c54fa59a72f00bfbb4c4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843315"
---
# <a name="comparegreaterthanfxp-operation"></a><span data-ttu-id="a7512-102">Operação CompareGreaterThanFxP</span><span class="sxs-lookup"><span data-stu-id="a7512-102">CompareGreaterThanFxP operation</span></span>

<span data-ttu-id="a7512-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a7512-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a7512-104">Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="a7512-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="a7512-105">Compara dois números de ponto fixo armazenados em registros de Quantum e controla uma inversão no resultado.</span><span class="sxs-lookup"><span data-stu-id="a7512-105">Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.</span></span>

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a7512-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7512-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="a7512-107">FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="a7512-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="a7512-108">Primeiro número de ponto fixo a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="a7512-108">First fixed-point number to be compared.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="a7512-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="a7512-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="a7512-110">Segundo número de ponto fixo a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="a7512-110">Second fixed-point number to be compared.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="a7512-111">resultado: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a7512-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a7512-112">Resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="a7512-112">Result of the comparison.</span></span> <span data-ttu-id="a7512-113">Será invertida se `fp1 > fp2` .</span><span class="sxs-lookup"><span data-stu-id="a7512-113">Will be flipped if `fp1 > fp2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a7512-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a7512-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a7512-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7512-115">Remarks</span></span>

<span data-ttu-id="a7512-116">A implementação atual requer que os dois números de ponto fixo tenham a mesma posição de ponto e o mesmo número de qubits.</span><span class="sxs-lookup"><span data-stu-id="a7512-116">The current implementation requires the two fixed-point numbers to have the same point position and the same number of qubits.</span></span>