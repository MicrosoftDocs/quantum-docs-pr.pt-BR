---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Operação AssertMeasurement
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 09024cd8cd6e713360dcf7f42f55941590f35883
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693560"
---
# <a name="assertmeasurement-operation"></a><span data-ttu-id="82ba2-102">Operação AssertMeasurement</span><span class="sxs-lookup"><span data-stu-id="82ba2-102">AssertMeasurement operation</span></span>

<span data-ttu-id="82ba2-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="82ba2-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="82ba2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="82ba2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="82ba2-105">As declarações que medem o qubits determinado na base de Pauli especificada sempre terão o resultado especificado.</span><span class="sxs-lookup"><span data-stu-id="82ba2-105">Asserts that measuring the given qubits in the given Pauli basis will always have the given result.</span></span>

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="82ba2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="82ba2-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="82ba2-107">bases: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="82ba2-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="82ba2-108">Um efeito de medida para declarar a probabilidade de, expresso como um operador qubit Pauli.</span><span class="sxs-lookup"><span data-stu-id="82ba2-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="82ba2-109">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="82ba2-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="82ba2-110">Um registro no qual fazer a asserção.</span><span class="sxs-lookup"><span data-stu-id="82ba2-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="82ba2-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="82ba2-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="82ba2-112">O resultado esperado de `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="82ba2-112">The expected result of `Measure(bases, qubits)`.</span></span>


### <a name="msg--string"></a><span data-ttu-id="82ba2-113">msg: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="82ba2-113">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="82ba2-114">Uma mensagem a ser relatada se a asserção falhar.</span><span class="sxs-lookup"><span data-stu-id="82ba2-114">A message to be reported if the assertion fails.</span></span>



## <a name="output--unit"></a><span data-ttu-id="82ba2-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82ba2-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="82ba2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="82ba2-116">Remarks</span></span>

<span data-ttu-id="82ba2-117">Observe que as versões adjacente e controladas dessa operação não verificarão a condição.</span><span class="sxs-lookup"><span data-stu-id="82ba2-117">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="82ba2-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="82ba2-118">See Also</span></span>

- [<span data-ttu-id="82ba2-119">Microsoft. Quantum. Diagnostics. AssertMeasurementProbability</span><span class="sxs-lookup"><span data-stu-id="82ba2-119">Microsoft.Quantum.Diagnostics.AssertMeasurementProbability</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)