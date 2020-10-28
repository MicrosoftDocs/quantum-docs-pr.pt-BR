---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Operação ApplyTransposition
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 1bd6f9580e09752f1de75927d6bb35417bb1ff21
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697060"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="101a8-102">Operação ApplyTransposition</span><span class="sxs-lookup"><span data-stu-id="101a8-102">ApplyTransposition operation</span></span>

<span data-ttu-id="101a8-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="101a8-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="101a8-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="101a8-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="101a8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="101a8-105">Description</span></span>

<span data-ttu-id="101a8-106">Esta operação alterna a amplitude no índice `a` com a amplitude no índice `b` no determinado estado-vetor de `register` tamanho $n $.</span><span class="sxs-lookup"><span data-stu-id="101a8-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="101a8-107">Se for `a` igual `b` a, o vetor de estado não será alterado.</span><span class="sxs-lookup"><span data-stu-id="101a8-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="101a8-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="101a8-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="101a8-109">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="101a8-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="101a8-110">Primeiro índice (deve ser um valor de 0 a $2 ^ n-$1)</span><span class="sxs-lookup"><span data-stu-id="101a8-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="101a8-111">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="101a8-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="101a8-112">O segundo índice (deve ser um valor de 0 a $2 ^ n-$1)</span><span class="sxs-lookup"><span data-stu-id="101a8-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="101a8-113">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="101a8-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="101a8-114">Uma lista de $n $ qubits à qual o transposição é aplicado.</span><span class="sxs-lookup"><span data-stu-id="101a8-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="101a8-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="101a8-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

