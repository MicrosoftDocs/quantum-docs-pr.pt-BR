---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlaceCompBasis
title: Operação AssertOperationsEqualInPlaceCompBasis
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlaceCompBasis
qsharp.summary: Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis. This is a necessary, but not sufficient, condition for the equality of two unitaries.
ms.openlocfilehash: 3275680f86ca2a178c7f044b97d226fe41c3186c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693550"
---
# <a name="assertoperationsequalinplacecompbasis-operation"></a><span data-ttu-id="8304d-102">Operação AssertOperationsEqualInPlaceCompBasis</span><span class="sxs-lookup"><span data-stu-id="8304d-102">AssertOperationsEqualInPlaceCompBasis operation</span></span>

<span data-ttu-id="8304d-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="8304d-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="8304d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8304d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8304d-105">Verifica se a operação `givenU` é igual à operação `expectedU` no tamanho de entrada fornecido, verificando a ação das operações somente nos vetores da base computacional.</span><span class="sxs-lookup"><span data-stu-id="8304d-105">Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis.</span></span>
<span data-ttu-id="8304d-106">Essa é uma condição necessária, mas não suficiente, para a igualdade de duas unidades.</span><span class="sxs-lookup"><span data-stu-id="8304d-106">This is a necessary, but not sufficient, condition for the equality of two unitaries.</span></span>

```qsharp
operation AssertOperationsEqualInPlaceCompBasis (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="8304d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8304d-107">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="8304d-108">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8304d-108">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8304d-109">O número de qubits $n $ em que as `givenU` operações `expectedU` funcionam.</span><span class="sxs-lookup"><span data-stu-id="8304d-109">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="8304d-110">dada: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="8304d-110">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8304d-111">Operação em $n $ qubits a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="8304d-111">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit-adj"></a><span data-ttu-id="8304d-112">expected: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8304d-112">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="8304d-113">Operação de referência em $n $ qubits que deve `givenU` ser comparada.</span><span class="sxs-lookup"><span data-stu-id="8304d-113">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8304d-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8304d-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

