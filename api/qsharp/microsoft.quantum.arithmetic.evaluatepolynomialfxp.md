---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Operação EvaluatePolynomialFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: 3903bf69d5b0a6e57530f2c6a44e1d351c8a605f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694795"
---
# <a name="evaluatepolynomialfxp-operation"></a><span data-ttu-id="ce34a-102">Operação EvaluatePolynomialFxP</span><span class="sxs-lookup"><span data-stu-id="ce34a-102">EvaluatePolynomialFxP operation</span></span>

<span data-ttu-id="ce34a-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ce34a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ce34a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ce34a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ce34a-105">Avalia um polinomial em uma representação de ponto fixo.</span><span class="sxs-lookup"><span data-stu-id="ce34a-105">Evaluates a polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="ce34a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce34a-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="ce34a-107">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ce34a-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ce34a-108">Coeficientes do polinomial como uma matriz Double, ou seja, a matriz $ [a_0, a_1,..., a_d] $ para o polinomial $P (x) = a_0 + a_1 x + \cdots + a_d x ^ d $.</span><span class="sxs-lookup"><span data-stu-id="ce34a-108">Coefficients of the polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_d]$ for the polynomial $P(x) = a_0 + a_1 x + \cdots + a_d x^d$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="ce34a-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="ce34a-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="ce34a-110">Número de ponto fixo de entrada para o qual avaliar o polinomial.</span><span class="sxs-lookup"><span data-stu-id="ce34a-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="ce34a-111">resultado: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="ce34a-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="ce34a-112">O número de ponto fixo de saída que irá manter $P (x) $.</span><span class="sxs-lookup"><span data-stu-id="ce34a-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="ce34a-113">Deve estar no estado $ \ket {0} $ inicialmente.</span><span class="sxs-lookup"><span data-stu-id="ce34a-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ce34a-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ce34a-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
