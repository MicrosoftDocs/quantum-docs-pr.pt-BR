---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Função MeasurementOperators
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 24d752c4f198764b6e7c6ea6c49669c020c1a502
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693652"
---
# <a name="measurementoperators-function"></a><span data-ttu-id="db2a1-102">Função MeasurementOperators</span><span class="sxs-lookup"><span data-stu-id="db2a1-102">MeasurementOperators function</span></span>

<span data-ttu-id="db2a1-103">Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="db2a1-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="db2a1-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="db2a1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="db2a1-105">Computa todos os operadores de medida necessários para computar a expectativa de um termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="db2a1-105">Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.</span></span>

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="db2a1-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="db2a1-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="db2a1-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="db2a1-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="db2a1-108">O número de qubits necessárias para simular o sistema molecular.</span><span class="sxs-lookup"><span data-stu-id="db2a1-108">The number of qubits required to simulate the molecular system.</span></span>


### <a name="indices--int"></a><span data-ttu-id="db2a1-109">índices: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="db2a1-109">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="db2a1-110">Uma matriz que contém os índices do qubit cada operador Pauli é aplicado a.</span><span class="sxs-lookup"><span data-stu-id="db2a1-110">An array containing the indices of the qubit each Pauli operator is applied to.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="db2a1-111">termtype: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="db2a1-111">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="db2a1-112">O tipo do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="db2a1-112">The type of the Jordan-Wigner term.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="db2a1-113">Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="db2a1-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="db2a1-114">Uma matriz de operadores de medida (cada um sendo uma matriz de Pauli).</span><span class="sxs-lookup"><span data-stu-id="db2a1-114">An array of measurement operators (each being an array of Pauli).</span></span>