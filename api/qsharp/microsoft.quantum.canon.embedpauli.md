---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: Função EmbedPauli
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: e9042ca9eac4b8791057037dc5698eb14deadd31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207030"
---
# <a name="embedpauli-function"></a><span data-ttu-id="be370-102">Função EmbedPauli</span><span class="sxs-lookup"><span data-stu-id="be370-102">EmbedPauli function</span></span>

<span data-ttu-id="be370-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="be370-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="be370-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="be370-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="be370-105">Dado um operador Pauli de qubit único e o índice de um qubit, retorna um operador Pauli de vários qubit com o operador Single-qubit fornecido nesse índice e `PauliI` em todos os outros índices.</span><span class="sxs-lookup"><span data-stu-id="be370-105">Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.</span></span>

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="be370-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="be370-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="be370-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="be370-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="be370-108">Um operador de Pauli de qubit único a ser colocado no local especificado.</span><span class="sxs-lookup"><span data-stu-id="be370-108">A single-qubit Pauli operator to be placed at the given location.</span></span>


### <a name="location--int"></a><span data-ttu-id="be370-109">local: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="be370-109">location : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="be370-110">Um índice de tal forma `output[location] == pauli` , em que `output` é a saída dessa função.</span><span class="sxs-lookup"><span data-stu-id="be370-110">An index such that `output[location] == pauli`, where `output` is the output of this function.</span></span>


### <a name="n--int"></a><span data-ttu-id="be370-111">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="be370-111">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="be370-112">Comprimento da matriz a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="be370-112">Length of the array to be returned.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="be370-113">Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="be370-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

