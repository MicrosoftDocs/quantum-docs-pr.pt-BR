---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Operação MultiplyFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 18883f3f4c3793b91e248f4bd89f9def640bf254
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694561"
---
# <a name="multiplyfxp-operation"></a><span data-ttu-id="32401-102">Operação MultiplyFxP</span><span class="sxs-lookup"><span data-stu-id="32401-102">MultiplyFxP operation</span></span>

<span data-ttu-id="32401-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="32401-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="32401-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="32401-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="32401-105">Multiplica dois números de ponto fixo em registros de Quantum.</span><span class="sxs-lookup"><span data-stu-id="32401-105">Multiplies two fixed-point numbers in quantum registers.</span></span>

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="32401-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="32401-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="32401-107">FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="32401-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="32401-108">Primeiro número de ponto fixo.</span><span class="sxs-lookup"><span data-stu-id="32401-108">First fixed-point number.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="32401-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="32401-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="32401-110">Segundo número de ponto fixo.</span><span class="sxs-lookup"><span data-stu-id="32401-110">Second fixed-point number.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="32401-111">resultado: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="32401-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="32401-112">Resultado número de ponto fixo, deve estar no estado $ \ket {0} $ inicialmente.</span><span class="sxs-lookup"><span data-stu-id="32401-112">Result fixed-point number, must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="32401-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="32401-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="32401-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="32401-114">Remarks</span></span>

<span data-ttu-id="32401-115">A implementação atual requer que os três números de ponto fixo tenham a mesma posição de ponto e o mesmo número de qubits.</span><span class="sxs-lookup"><span data-stu-id="32401-115">The current implementation requires the three fixed-point numbers to have the same point position and the same number of qubits.</span></span>