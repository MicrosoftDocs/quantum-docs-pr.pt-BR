---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Função _DeltaParityCNOTbitstring
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 0c0da60e3c389f8208f9f7d5c84a09893f3c1bda
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226070"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="50b48-102">Função _DeltaParityCNOTbitstring</span><span class="sxs-lookup"><span data-stu-id="50b48-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="50b48-103">Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="50b48-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="50b48-104">Pacote: [Microsoft. Quantum. Research. química](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="50b48-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="50b48-105">Etapa de processamento clássico de `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="50b48-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="50b48-106">Isso computa uma lista de qubits de controle para avaliar a diferença de paridade entre duas PQRS... termos de comprimento par.</span><span class="sxs-lookup"><span data-stu-id="50b48-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="50b48-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="50b48-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="50b48-108">prevFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="50b48-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="50b48-109">nextFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="50b48-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="50b48-110">Saída: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="50b48-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="50b48-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="50b48-111">Remarks</span></span>

<span data-ttu-id="50b48-112">Isso pressupõe que o comprimento dos termos é par.</span><span class="sxs-lookup"><span data-stu-id="50b48-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="50b48-113">Computa a lista de controles para diferença de paridade entre dois termos.</span><span class="sxs-lookup"><span data-stu-id="50b48-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="50b48-114">Isso pressupõe que as listas de entrada são classificadas em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="50b48-114">This assumes that the input lists is sorted in ascending order.</span></span>