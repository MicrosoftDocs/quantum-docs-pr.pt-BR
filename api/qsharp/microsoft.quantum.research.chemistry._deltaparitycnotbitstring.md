---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Função _DeltaParityCNOTbitstring
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 3dd2d299a094577d377780d731e76287815e8d03
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847594"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="d798f-102">Função _DeltaParityCNOTbitstring</span><span class="sxs-lookup"><span data-stu-id="d798f-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="d798f-103">Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d798f-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="d798f-104">Pacote: [Microsoft. Quantum. Research. química](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d798f-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="d798f-105">Etapa de processamento clássico de `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="d798f-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="d798f-106">Isso computa uma lista de qubits de controle para avaliar a diferença de paridade entre duas PQRS... termos de comprimento par.</span><span class="sxs-lookup"><span data-stu-id="d798f-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="d798f-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d798f-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="d798f-108">prevFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d798f-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="d798f-109">nextFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d798f-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="d798f-110">Saída: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="d798f-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="d798f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d798f-111">Remarks</span></span>

<span data-ttu-id="d798f-112">Isso pressupõe que o comprimento dos termos é par.</span><span class="sxs-lookup"><span data-stu-id="d798f-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="d798f-113">Computa a lista de controles para diferença de paridade entre dois termos.</span><span class="sxs-lookup"><span data-stu-id="d798f-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="d798f-114">Isso pressupõe que as listas de entrada são classificadas em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="d798f-114">This assumes that the input lists is sorted in ascending order.</span></span>