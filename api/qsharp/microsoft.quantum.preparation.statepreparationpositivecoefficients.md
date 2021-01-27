---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Função StatePreparationPositiveCoefficients
ms.date: 1/23/2021 12:00:00 AM
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
ms.openlocfilehash: 081541d93bf853fa0de1573038dc00c296432281
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855855"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="9a3e1-102">Função StatePreparationPositiveCoefficients</span><span class="sxs-lookup"><span data-stu-id="9a3e1-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="9a3e1-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="9a3e1-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="9a3e1-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9a3e1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="9a3e1-105">StatePreparationPositiveCoefficients foi preterido.</span><span class="sxs-lookup"><span data-stu-id="9a3e1-105">StatePreparationPositiveCoefficients has been deprecated.</span></span> <span data-ttu-id="9a3e1-106">Use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="9a3e1-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.</span></span>

<span data-ttu-id="9a3e1-107">Retorna uma operação que prepara o estado de Quantum fornecido.</span><span class="sxs-lookup"><span data-stu-id="9a3e1-107">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="9a3e1-108">A operação retornada $U $ prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes positivos $ \ alpha_j \ge $0 do estado de base computacional $n $-qubit $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="9a3e1-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="9a3e1-109">A ação de U em um registro recém-alocado é fornecida por $ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="9a3e1-109">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="9a3e1-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="9a3e1-110">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="9a3e1-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a3e1-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="9a3e1-112">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9a3e1-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9a3e1-113">Matriz de até $2 ^ n $ coeficientes $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="9a3e1-113">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="9a3e1-114">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="9a3e1-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="9a3e1-115">Saída: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="9a3e1-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="9a3e1-116">Uma operação unitário de preparação de estado $U $.</span><span class="sxs-lookup"><span data-stu-id="9a3e1-116">A state-preparation unitary operation $U$.</span></span>

## <a name="example"></a><span data-ttu-id="9a3e1-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9a3e1-117">Example</span></span>

<span data-ttu-id="9a3e1-118">O trecho a seguir prepara o estado Quantum $ \ket{\psi} = \ sqrt {1/8} \ ket {0} + \ sqrt {7/8} \ ket {2} $ no registro qubit `qubitsLE` .</span><span class="sxs-lookup"><span data-stu-id="9a3e1-118">The following snippet prepares the quantum state $\ket{\psi}=\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{2}$ in the qubit register `qubitsLE`.</span></span>

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let op = StatePreparationPositiveCoefficients(amplitudes);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a><span data-ttu-id="9a3e1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a3e1-119">Remarks</span></span>

<span data-ttu-id="9a3e1-120">Os coeficientes de entrada negativos $ \ alpha_j < $0 serão tratados como se positivo com o valor $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="9a3e1-120">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="9a3e1-121">`coefficients` será preenchido com os elementos $ \ alpha_j = $0 se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="9a3e1-121">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>