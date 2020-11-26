---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Função StatePreparationPositiveCoefficients
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationPositiveCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.


  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 8f1fd7d77531996faf566adb78f452929d6cbd50
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193243"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="94943-102">Função StatePreparationPositiveCoefficients</span><span class="sxs-lookup"><span data-stu-id="94943-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="94943-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="94943-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="94943-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="94943-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="94943-105">StatePreparationPositiveCoefficients foi preterido.</span><span class="sxs-lookup"><span data-stu-id="94943-105">StatePreparationPositiveCoefficients has been deprecated.</span></span> <span data-ttu-id="94943-106">Use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="94943-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.</span></span>

<span data-ttu-id="94943-107">Retorna uma operação que prepara o estado de Quantum fornecido.</span><span class="sxs-lookup"><span data-stu-id="94943-107">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="94943-108">A operação retornada $U $ prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes positivos $ \ alpha_j \ge $0 do estado de base computacional $n $-qubit $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="94943-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="94943-109">A ação de U em um registro recém-alocado é fornecida por $ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="94943-109">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="94943-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="94943-110">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="94943-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="94943-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="94943-112">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="94943-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="94943-113">Matriz de até $2 ^ n $ coeficientes $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="94943-113">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="94943-114">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="94943-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="94943-115">Saída: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="94943-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="94943-116">Uma operação unitário de preparação de estado $U $.</span><span class="sxs-lookup"><span data-stu-id="94943-116">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="94943-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="94943-117">Remarks</span></span>

<span data-ttu-id="94943-118">Os coeficientes de entrada negativos $ \ alpha_j < $0 serão tratados como se positivo com o valor $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="94943-118">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="94943-119">`coefficients` será preenchido com os elementos $ \ alpha_j = $0 se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="94943-119">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>