---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Função StatePreparationPositiveCoefficients
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 39d961c71d231e7b51290f81c20c8c6b48c7e0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92695052"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="9d43b-102">Função StatePreparationPositiveCoefficients</span><span class="sxs-lookup"><span data-stu-id="9d43b-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="9d43b-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="9d43b-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="9d43b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9d43b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9d43b-105">Retorna uma operação que prepara o estado de Quantum fornecido.</span><span class="sxs-lookup"><span data-stu-id="9d43b-105">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="9d43b-106">A operação retornada $U $ prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes positivos $ \ alpha_j \ge $0 do estado de base computacional $n $-qubit $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="9d43b-106">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="9d43b-107">A ação de U em um registro recém-alocado é fornecida por $ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="9d43b-107">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="9d43b-108">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="9d43b-108">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="9d43b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="9d43b-109">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="9d43b-110">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9d43b-110">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9d43b-111">Matriz de até $2 ^ n $ coeficientes $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="9d43b-111">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="9d43b-112">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="9d43b-112">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit-adj--ctl"></a><span data-ttu-id="9d43b-113">Saída: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) da => [unidade](xref:microsoft.quantum.lang-ref.unit) do ano + CTL</span><span class="sxs-lookup"><span data-stu-id="9d43b-113">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="9d43b-114">Uma operação unitário de preparação de estado $U $.</span><span class="sxs-lookup"><span data-stu-id="9d43b-114">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d43b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d43b-115">Remarks</span></span>

<span data-ttu-id="9d43b-116">Os coeficientes de entrada negativos $ \ alpha_j < $0 serão tratados como se positivo com o valor $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="9d43b-116">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="9d43b-117">`coefficients` será preenchido com os elementos $ \ alpha_j = $0 se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="9d43b-117">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>