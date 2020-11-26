---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Operação ApplyTransposition
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: ca22b090f2b2613f07caef698941ea608374ab1e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203307"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="f7737-102">Operação ApplyTransposition</span><span class="sxs-lookup"><span data-stu-id="f7737-102">ApplyTransposition operation</span></span>

<span data-ttu-id="f7737-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="f7737-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="f7737-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f7737-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="f7737-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7737-105">Description</span></span>

<span data-ttu-id="f7737-106">Esta operação alterna a amplitude no índice `a` com a amplitude no índice `b` no determinado estado-vetor de `register` tamanho $n $.</span><span class="sxs-lookup"><span data-stu-id="f7737-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="f7737-107">Se for `a` igual `b` a, o vetor de estado não será alterado.</span><span class="sxs-lookup"><span data-stu-id="f7737-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="f7737-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7737-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="f7737-109">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f7737-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f7737-110">Primeiro índice (deve ser um valor de 0 a $2 ^ n-$1)</span><span class="sxs-lookup"><span data-stu-id="f7737-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="f7737-111">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f7737-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f7737-112">O segundo índice (deve ser um valor de 0 a $2 ^ n-$1)</span><span class="sxs-lookup"><span data-stu-id="f7737-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="f7737-113">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f7737-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f7737-114">Uma lista de $n $ qubits à qual o transposição é aplicado.</span><span class="sxs-lookup"><span data-stu-id="f7737-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f7737-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f7737-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

