---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Operação AssertMeasurementProbability
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 2fd89121516ef6994dedb75b214589b4e360ff8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830833"
---
# <a name="assertmeasurementprobability-operation"></a><span data-ttu-id="48334-102">Operação AssertMeasurementProbability</span><span class="sxs-lookup"><span data-stu-id="48334-102">AssertMeasurementProbability operation</span></span>

<span data-ttu-id="48334-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="48334-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="48334-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="48334-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="48334-105">As declarações que medem o qubits determinado na base de Pauli especificada terão o resultado fornecido com a probabilidade determinada, dentro de certa tolerância.</span><span class="sxs-lookup"><span data-stu-id="48334-105">Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="48334-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="48334-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="48334-107">bases: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="48334-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="48334-108">Um efeito de medida para declarar a probabilidade de, expresso como um operador qubit Pauli.</span><span class="sxs-lookup"><span data-stu-id="48334-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="48334-109">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="48334-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="48334-110">Um registro no qual fazer a asserção.</span><span class="sxs-lookup"><span data-stu-id="48334-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="48334-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="48334-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="48334-112">Um resultado esperado de `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="48334-112">An expected result of `Measure(bases, qubits)`.</span></span>


### <a name="prob--double"></a><span data-ttu-id="48334-113">prob: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="48334-113">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="48334-114">A probabilidade com a qual o resultado especificado é esperado.</span><span class="sxs-lookup"><span data-stu-id="48334-114">The probability with which the given result is expected.</span></span>


### <a name="msg--string"></a><span data-ttu-id="48334-115">msg: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="48334-115">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="48334-116">Uma mensagem a ser relatada se a asserção falhar.</span><span class="sxs-lookup"><span data-stu-id="48334-116">A message to be reported if the assertion fails.</span></span>


### <a name="tol--double"></a><span data-ttu-id="48334-117">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="48334-117">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="48334-118">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="48334-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="48334-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="48334-119">Example</span></span>

```qsharp
using (register = Qubit()) {
    H(register);
    AssertProb([PauliZ], [register], One, 0.5,
        "Measuring in conjugate basis did not give 50/50 results.", 1e-5);
}
```

## <a name="remarks"></a><span data-ttu-id="48334-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="48334-120">Remarks</span></span>

<span data-ttu-id="48334-121">Observe que as versões adjacente e controladas dessa operação não verificarão a condição.</span><span class="sxs-lookup"><span data-stu-id="48334-121">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="48334-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="48334-122">See Also</span></span>

- [<span data-ttu-id="48334-123">Microsoft. Quantum. Diagnostics. AssertMeasurement</span><span class="sxs-lookup"><span data-stu-id="48334-123">Microsoft.Quantum.Diagnostics.AssertMeasurement</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)