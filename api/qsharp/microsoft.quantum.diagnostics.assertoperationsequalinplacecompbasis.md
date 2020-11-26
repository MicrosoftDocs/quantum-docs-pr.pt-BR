---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlaceCompBasis
title: Operação AssertOperationsEqualInPlaceCompBasis
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlaceCompBasis
qsharp.summary: Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis. This is a necessary, but not sufficient, condition for the equality of two unitaries.
ms.openlocfilehash: 826369bdf3544fb257c2bb202466426c1ca1e113
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202338"
---
# <a name="assertoperationsequalinplacecompbasis-operation"></a><span data-ttu-id="9b7d8-102">Operação AssertOperationsEqualInPlaceCompBasis</span><span class="sxs-lookup"><span data-stu-id="9b7d8-102">AssertOperationsEqualInPlaceCompBasis operation</span></span>

<span data-ttu-id="9b7d8-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="9b7d8-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="9b7d8-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9b7d8-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9b7d8-105">Verifica se a operação `givenU` é igual à operação `expectedU` no tamanho de entrada fornecido, verificando a ação das operações somente nos vetores da base computacional.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-105">Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis.</span></span>
<span data-ttu-id="9b7d8-106">Essa é uma condição necessária, mas não suficiente, para a igualdade de duas unidades.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-106">This is a necessary, but not sufficient, condition for the equality of two unitaries.</span></span>

```qsharp
operation AssertOperationsEqualInPlaceCompBasis (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="9b7d8-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b7d8-107">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="9b7d8-108">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9b7d8-108">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9b7d8-109">O número de qubits $n $ em que as `givenU` operações `expectedU` funcionam.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-109">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="9b7d8-110">dada: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="9b7d8-110">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="9b7d8-111">Operação em $n $ qubits a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-111">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="9b7d8-112">expectedd: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="9b7d8-112">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="9b7d8-113">Operação de referência em $n $ qubits que deve `givenU` ser comparada.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-113">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9b7d8-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9b7d8-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

