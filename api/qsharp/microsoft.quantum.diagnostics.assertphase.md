---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Operação AssertPhase
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 9130d6c735d90abbc51989ef4a68a8eff8b41371
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202253"
---
# <a name="assertphase-operation"></a><span data-ttu-id="2a5d4-102">Operação AssertPhase</span><span class="sxs-lookup"><span data-stu-id="2a5d4-102">AssertPhase operation</span></span>

<span data-ttu-id="2a5d4-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="2a5d4-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="2a5d4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2a5d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2a5d4-105">Declara que a fase de um estado de superposição igual tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="2a5d4-105">Asserts that the phase of an equal superposition state has the expected value.</span></span>

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="2a5d4-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a5d4-106">Description</span></span>

<span data-ttu-id="2a5d4-107">Esta operação declara que a fase $ \phi $ de um estado Quantum que pode ser expressa como $ \frac{e ^ {i t}} {\sqrt {2} } (e ^ {i\phi} \ ket {0} + e ^ {-i\phi} \ ket {1} ) $ para algum real $t $ arbitrário tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="2a5d4-107">This operation asserts that the phase $\phi$ of a quantum state that may be expressed as $\frac{e^{i t}}{\sqrt{2}}(e^{i\phi}\ket{0} + e^{-i\phi}\ket{1})$ for some arbitrary real $t$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="2a5d4-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a5d4-108">Input</span></span>

### <a name="expected--double"></a><span data-ttu-id="2a5d4-109">esperado: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2a5d4-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2a5d4-110">O valor esperado de $ \phi na (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="2a5d4-110">The expected value of $\phi \in (-\pi,\pi]$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="2a5d4-111">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2a5d4-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2a5d4-112">O qubit que armazena o estado esperado.</span><span class="sxs-lookup"><span data-stu-id="2a5d4-112">The qubit that stores the expected state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="2a5d4-113">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2a5d4-113">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2a5d4-114">Tolerância absoluta na diferença entre real e esperado.</span><span class="sxs-lookup"><span data-stu-id="2a5d4-114">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2a5d4-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2a5d4-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

