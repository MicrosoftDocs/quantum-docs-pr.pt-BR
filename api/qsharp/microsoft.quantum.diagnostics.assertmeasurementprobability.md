---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Operação AssertMeasurementProbability
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 032b9224ad728f0637596668c2928a889deeba55
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202355"
---
# <a name="assertmeasurementprobability-operation"></a><span data-ttu-id="fe378-102">Operação AssertMeasurementProbability</span><span class="sxs-lookup"><span data-stu-id="fe378-102">AssertMeasurementProbability operation</span></span>

<span data-ttu-id="fe378-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="fe378-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="fe378-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="fe378-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="fe378-105">As declarações que medem o qubits determinado na base de Pauli especificada terão o resultado fornecido com a probabilidade determinada, dentro de certa tolerância.</span><span class="sxs-lookup"><span data-stu-id="fe378-105">Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="fe378-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe378-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="fe378-107">bases: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="fe378-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="fe378-108">Um efeito de medida para declarar a probabilidade de, expresso como um operador qubit Pauli.</span><span class="sxs-lookup"><span data-stu-id="fe378-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="fe378-109">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fe378-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fe378-110">Um registro no qual fazer a asserção.</span><span class="sxs-lookup"><span data-stu-id="fe378-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="fe378-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="fe378-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="fe378-112">Um resultado esperado de `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="fe378-112">An expected result of `Measure(bases, qubits)`.</span></span>


### <a name="prob--double"></a><span data-ttu-id="fe378-113">prob: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fe378-113">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fe378-114">A probabilidade com a qual o resultado especificado é esperado.</span><span class="sxs-lookup"><span data-stu-id="fe378-114">The probability with which the given result is expected.</span></span>


### <a name="msg--string"></a><span data-ttu-id="fe378-115">msg: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="fe378-115">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="fe378-116">Uma mensagem a ser relatada se a asserção falhar.</span><span class="sxs-lookup"><span data-stu-id="fe378-116">A message to be reported if the assertion fails.</span></span>


### <a name="tol--double"></a><span data-ttu-id="fe378-117">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fe378-117">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="fe378-118">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fe378-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fe378-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe378-119">Remarks</span></span>

<span data-ttu-id="fe378-120">Observe que as versões adjacente e controladas dessa operação não verificarão a condição.</span><span class="sxs-lookup"><span data-stu-id="fe378-120">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe378-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fe378-121">See Also</span></span>

- [<span data-ttu-id="fe378-122">Microsoft. Quantum. Diagnostics. AssertMeasurement</span><span class="sxs-lookup"><span data-stu-id="fe378-122">Microsoft.Quantum.Diagnostics.AssertMeasurement</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)