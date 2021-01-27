---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Operação MeasureStabilizerGenerators
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: d7c8df079e49b2ce0a5106e430ef4060df85cdc4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825767"
---
# <a name="measurestabilizergenerators-operation"></a><span data-ttu-id="66a3b-102">Operação MeasureStabilizerGenerators</span><span class="sxs-lookup"><span data-stu-id="66a3b-102">MeasureStabilizerGenerators operation</span></span>

<span data-ttu-id="66a3b-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="66a3b-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="66a3b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66a3b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66a3b-105">Mede o conjunto determinado de geradores de um grupo de estabilizador.</span><span class="sxs-lookup"><span data-stu-id="66a3b-105">Measures the given set of generators of a stabilizer group.</span></span>

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a><span data-ttu-id="66a3b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="66a3b-106">Input</span></span>

### <a name="stabilizergroup--pauli"></a><span data-ttu-id="66a3b-107">stabilizerGroup: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="66a3b-107">stabilizerGroup : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="66a3b-108">Uma matriz de operadores multiqubit Pauli.</span><span class="sxs-lookup"><span data-stu-id="66a3b-108">An array of multiqubit Pauli operators.</span></span>
<span data-ttu-id="66a3b-109">Por exemplo, `stabilizerGroup[0]` é uma lista de matrizes de Pauli de qubit único, o produto tensor do qual é um gerador de estabilizador.</span><span class="sxs-lookup"><span data-stu-id="66a3b-109">For example, `stabilizerGroup[0]` is a list of single-qubit Pauli matrices, the tensor product of which is a stabilizer generator.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="66a3b-110">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="66a3b-110">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="66a3b-111">Uma matriz de qubits onde o código de estabilizador é definido.</span><span class="sxs-lookup"><span data-stu-id="66a3b-111">An array of qubits where the stabilizer code is defined.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="66a3b-112">gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="66a3b-112">gadget : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="66a3b-113">Uma operação que especifica como medir um operador multiqubit Pauli.</span><span class="sxs-lookup"><span data-stu-id="66a3b-113">An operation that specifies how to measure a multiqubit Pauli operator.</span></span>



## <a name="output--syndrome"></a><span data-ttu-id="66a3b-114">Saída: [síndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="66a3b-114">Output : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="66a3b-115">O resultado de medições.</span><span class="sxs-lookup"><span data-stu-id="66a3b-115">The result of measurements.</span></span>

## <a name="remarks"></a><span data-ttu-id="66a3b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="66a3b-116">Remarks</span></span>

<span data-ttu-id="66a3b-117">Isso não verifica se o conjunto determinado de geradores está em comutação.</span><span class="sxs-lookup"><span data-stu-id="66a3b-117">This does not check if the given set of generators are commuting.</span></span>
<span data-ttu-id="66a3b-118">Se não estiverem em comutação, o resultado das medições poderá ser arbitrário.</span><span class="sxs-lookup"><span data-stu-id="66a3b-118">If they are not commuting, the result of measurements may be arbitrary.</span></span>