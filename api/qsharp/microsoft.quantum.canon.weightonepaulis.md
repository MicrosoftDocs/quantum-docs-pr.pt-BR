---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: Função WeightOnePaulis
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 89802c1bc6f3da8edef27b698eb61098e47dfc85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693869"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="24397-102">Função WeightOnePaulis</span><span class="sxs-lookup"><span data-stu-id="24397-102">WeightOnePaulis function</span></span>

<span data-ttu-id="24397-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="24397-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="24397-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="24397-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="24397-105">Retorna uma matriz de todos os operadores de Pauli peso-1 em um determinado número de qubits.</span><span class="sxs-lookup"><span data-stu-id="24397-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="24397-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="24397-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="24397-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="24397-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="24397-108">O número de qubits em que os operadores de Pauli retornados são definidos.</span><span class="sxs-lookup"><span data-stu-id="24397-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="24397-109">Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="24397-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="24397-110">Uma matriz de operadores qubit Pauli, cada um dos quais é representado como uma matriz com comprimento `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="24397-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>