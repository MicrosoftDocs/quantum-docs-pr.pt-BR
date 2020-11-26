---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: Operação AssertOperationsEqualInPlace
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 9b17bac9d95baf5a542604892c64130bf35d7f69
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202423"
---
# <a name="assertoperationsequalinplace-operation"></a><span data-ttu-id="a2454-102">Operação AssertOperationsEqualInPlace</span><span class="sxs-lookup"><span data-stu-id="a2454-102">AssertOperationsEqualInPlace operation</span></span>

<span data-ttu-id="a2454-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="a2454-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="a2454-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a2454-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a2454-105">Dadas duas operações, afirma que elas agem de forma idêntica para todos os Estados de entrada.</span><span class="sxs-lookup"><span data-stu-id="a2454-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="a2454-106">Essa asserção é implementada verificando a ação das operações em todos os Estados do formulário $V _0 \otimes... \otimes V_ {n-1} $, em que $V _k $ é um dos Estados $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ e $ \ket{i} $ (+ 1 eigenstate do operador Y Pauli).</span><span class="sxs-lookup"><span data-stu-id="a2454-106">This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).</span></span>

<span data-ttu-id="a2454-107">Essa declaração usa $n $ qubits e requer que várias chamadas das operações sejam comparadas.</span><span class="sxs-lookup"><span data-stu-id="a2454-107">This assertion uses $n$ qubits and requires multiple calls of the operations being compared.</span></span>

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="a2454-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2454-108">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="a2454-109">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a2454-109">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a2454-110">O número de qubits $n $ em que as `givenU` operações `expectedU` funcionam.</span><span class="sxs-lookup"><span data-stu-id="a2454-110">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="a2454-111">dada: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="a2454-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a2454-112">Operação em $n $ qubits a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="a2454-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="a2454-113">expectedd: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="a2454-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="a2454-114">Operação de referência em $n $ qubits que deve `givenU` ser comparada.</span><span class="sxs-lookup"><span data-stu-id="a2454-114">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a2454-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a2454-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="a2454-116">Referências</span><span class="sxs-lookup"><span data-stu-id="a2454-116">References</span></span>

<span data-ttu-id="a2454-117">A base dos Estados $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ e $ \ket{i} $ é a base Chuang-Nielsen, descrita em [ *i. L. Chuang, M. A. Nielsen*](https://arxiv.org/abs/quant-ph/9610001).</span><span class="sxs-lookup"><span data-stu-id="a2454-117">The basis of states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ is the Chuang-Nielsen basis, described in [ *I. L. Chuang, M. A. Nielsen* ](https://arxiv.org/abs/quant-ph/9610001).</span></span>

## <a name="see-also"></a><span data-ttu-id="a2454-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a2454-118">See Also</span></span>

- [<span data-ttu-id="a2454-119">Microsoft. Quantum. Diagnostics. AssertOperationsEqualReferenced</span><span class="sxs-lookup"><span data-stu-id="a2454-119">Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)