---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Operação AssertQubitWithinTolerance
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 7f57fc7a29d3eb86dc94cb24230d52b37eb6971d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853426"
---
# <a name="assertqubitwithintolerance-operation"></a><span data-ttu-id="b1330-102">Operação AssertQubitWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="b1330-102">AssertQubitWithinTolerance operation</span></span>

<span data-ttu-id="b1330-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="b1330-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="b1330-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b1330-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b1330-105">Declara que o qubit `q` está no eigenstate esperado do operador Z Pauli até uma determinada tolerância.</span><span class="sxs-lookup"><span data-stu-id="b1330-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.</span></span>

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="b1330-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1330-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="b1330-107">esperado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="b1330-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="b1330-108">Em que estado o qubit deve estar: `Zero` ou `One` .</span><span class="sxs-lookup"><span data-stu-id="b1330-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="b1330-109">p: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b1330-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b1330-110">O qubit cujo estado é declarado.</span><span class="sxs-lookup"><span data-stu-id="b1330-110">The qubit whose state is asserted.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="b1330-111">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b1330-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b1330-112">Tolerância na probabilidade de uma medida do qubit que retorna o resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="b1330-112">Tolerance on the probability of a measurement of the qubit returning the expected result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b1330-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b1330-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b1330-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1330-114">Remarks</span></span>

<span data-ttu-id="b1330-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> permite declarar Estados qubit arbitrários em vez de apenas $Z $ eigenstates.</span><span class="sxs-lookup"><span data-stu-id="b1330-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1330-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b1330-116">See Also</span></span>

- [<span data-ttu-id="b1330-117">Microsoft. Quantum. Diagnostics. AssertQubitIsInStateWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="b1330-117">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)