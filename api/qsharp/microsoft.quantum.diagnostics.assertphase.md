---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Operação AssertPhase
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: e042c03d2a72d9ce4816a8cdb56603e175b22807
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693548"
---
# <a name="assertphase-operation"></a><span data-ttu-id="7fd6f-102">Operação AssertPhase</span><span class="sxs-lookup"><span data-stu-id="7fd6f-102">AssertPhase operation</span></span>

<span data-ttu-id="7fd6f-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="7fd6f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="7fd6f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7fd6f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7fd6f-105">Declara que a fase de um estado de superposição igual tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="7fd6f-105">Asserts that the phase of an equal superposition state has the expected value.</span></span>

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="7fd6f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fd6f-106">Description</span></span>

<span data-ttu-id="7fd6f-107">Esta operação declara que a fase $ \phi $ de um estado Quantum que pode ser expressa como $ \frac{e ^ {i t}} {\sqrt {2} } (e ^ {i\phi} \ ket {0} + e ^ {-i\phi} \ ket {1} ) $ para algum real $t $ arbitrário tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="7fd6f-107">This operation asserts that the phase $\phi$ of a quantum state that may be expressed as $\frac{e^{i t}}{\sqrt{2}}(e^{i\phi}\ket{0} + e^{-i\phi}\ket{1})$ for some arbitrary real $t$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="7fd6f-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="7fd6f-108">Input</span></span>

### <a name="expected--double"></a><span data-ttu-id="7fd6f-109">esperado: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7fd6f-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7fd6f-110">O valor esperado de $ \phi na (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="7fd6f-110">The expected value of $\phi \in (-\pi,\pi]$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="7fd6f-111">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7fd6f-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7fd6f-112">O qubit que armazena o estado esperado.</span><span class="sxs-lookup"><span data-stu-id="7fd6f-112">The qubit that stores the expected state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="7fd6f-113">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7fd6f-113">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7fd6f-114">Tolerância absoluta na diferença entre real e esperado.</span><span class="sxs-lookup"><span data-stu-id="7fd6f-114">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7fd6f-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7fd6f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

