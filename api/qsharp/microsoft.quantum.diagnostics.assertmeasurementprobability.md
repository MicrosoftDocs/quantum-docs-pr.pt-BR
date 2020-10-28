---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Operação AssertMeasurementProbability
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: ff0419706d825442492f82e564f1cce86f1b112f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693552"
---
# <a name="assertmeasurementprobability-operation"></a><span data-ttu-id="f4ca6-102">Operação AssertMeasurementProbability</span><span class="sxs-lookup"><span data-stu-id="f4ca6-102">AssertMeasurementProbability operation</span></span>

<span data-ttu-id="f4ca6-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f4ca6-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f4ca6-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f4ca6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f4ca6-105">As declarações que medem o qubits determinado na base de Pauli especificada terão o resultado fornecido com a probabilidade determinada, dentro de certa tolerância.</span><span class="sxs-lookup"><span data-stu-id="f4ca6-105">Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="f4ca6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4ca6-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="f4ca6-107">bases: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="f4ca6-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="f4ca6-108">Um efeito de medida para declarar a probabilidade de, expresso como um operador qubit Pauli.</span><span class="sxs-lookup"><span data-stu-id="f4ca6-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="f4ca6-109">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f4ca6-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f4ca6-110">Um registro no qual fazer a asserção.</span><span class="sxs-lookup"><span data-stu-id="f4ca6-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="f4ca6-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="f4ca6-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="f4ca6-112">Um resultado esperado de `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="f4ca6-112">An expected result of `Measure(bases, qubits)`.</span></span>


### <a name="prob--double"></a><span data-ttu-id="f4ca6-113">prob: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f4ca6-113">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f4ca6-114">A probabilidade com a qual o resultado especificado é esperado.</span><span class="sxs-lookup"><span data-stu-id="f4ca6-114">The probability with which the given result is expected.</span></span>


### <a name="msg--string"></a><span data-ttu-id="f4ca6-115">msg: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="f4ca6-115">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="f4ca6-116">Uma mensagem a ser relatada se a asserção falhar.</span><span class="sxs-lookup"><span data-stu-id="f4ca6-116">A message to be reported if the assertion fails.</span></span>


### <a name="tol--double"></a><span data-ttu-id="f4ca6-117">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f4ca6-117">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="f4ca6-118">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f4ca6-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f4ca6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4ca6-119">Remarks</span></span>

<span data-ttu-id="f4ca6-120">Observe que as versões adjacente e controladas dessa operação não verificarão a condição.</span><span class="sxs-lookup"><span data-stu-id="f4ca6-120">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4ca6-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f4ca6-121">See Also</span></span>

- [<span data-ttu-id="f4ca6-122">Microsoft. Quantum. Diagnostics. AssertMeasurement</span><span class="sxs-lookup"><span data-stu-id="f4ca6-122">Microsoft.Quantum.Diagnostics.AssertMeasurement</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)