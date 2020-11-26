---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Operação AssertMeasurement
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 3fbe000202abbd8a206b0c83dfa35f4546ea91cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202440"
---
# <a name="assertmeasurement-operation"></a><span data-ttu-id="9c46f-102">Operação AssertMeasurement</span><span class="sxs-lookup"><span data-stu-id="9c46f-102">AssertMeasurement operation</span></span>

<span data-ttu-id="9c46f-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="9c46f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="9c46f-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9c46f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9c46f-105">As declarações que medem o qubits determinado na base de Pauli especificada sempre terão o resultado especificado.</span><span class="sxs-lookup"><span data-stu-id="9c46f-105">Asserts that measuring the given qubits in the given Pauli basis will always have the given result.</span></span>

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9c46f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c46f-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="9c46f-107">bases: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="9c46f-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="9c46f-108">Um efeito de medida para declarar a probabilidade de, expresso como um operador qubit Pauli.</span><span class="sxs-lookup"><span data-stu-id="9c46f-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="9c46f-109">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9c46f-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9c46f-110">Um registro no qual fazer a asserção.</span><span class="sxs-lookup"><span data-stu-id="9c46f-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="9c46f-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="9c46f-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="9c46f-112">O resultado esperado de `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="9c46f-112">The expected result of `Measure(bases, qubits)`.</span></span>


### <a name="msg--string"></a><span data-ttu-id="9c46f-113">msg: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="9c46f-113">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="9c46f-114">Uma mensagem a ser relatada se a asserção falhar.</span><span class="sxs-lookup"><span data-stu-id="9c46f-114">A message to be reported if the assertion fails.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9c46f-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9c46f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9c46f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c46f-116">Remarks</span></span>

<span data-ttu-id="9c46f-117">Observe que as versões adjacente e controladas dessa operação não verificarão a condição.</span><span class="sxs-lookup"><span data-stu-id="9c46f-117">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c46f-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9c46f-118">See Also</span></span>

- [<span data-ttu-id="9c46f-119">Microsoft. Quantum. Diagnostics. AssertMeasurementProbability</span><span class="sxs-lookup"><span data-stu-id="9c46f-119">Microsoft.Quantum.Diagnostics.AssertMeasurementProbability</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)