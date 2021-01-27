---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Função MeasurementOperators
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 204ae621b77559a894f0bce14e494824d58e4ad6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835392"
---
# <a name="measurementoperators-function"></a><span data-ttu-id="52c13-102">Função MeasurementOperators</span><span class="sxs-lookup"><span data-stu-id="52c13-102">MeasurementOperators function</span></span>

<span data-ttu-id="52c13-103">Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="52c13-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="52c13-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="52c13-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="52c13-105">Computa todos os operadores de medida necessários para computar a expectativa de um termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="52c13-105">Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.</span></span>

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="52c13-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="52c13-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="52c13-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="52c13-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="52c13-108">O número de qubits necessárias para simular o sistema molecular.</span><span class="sxs-lookup"><span data-stu-id="52c13-108">The number of qubits required to simulate the molecular system.</span></span>


### <a name="indices--int"></a><span data-ttu-id="52c13-109">índices: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="52c13-109">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="52c13-110">Uma matriz que contém os índices do qubit cada operador Pauli é aplicado a.</span><span class="sxs-lookup"><span data-stu-id="52c13-110">An array containing the indices of the qubit each Pauli operator is applied to.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="52c13-111">termtype: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="52c13-111">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="52c13-112">O tipo do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="52c13-112">The type of the Jordan-Wigner term.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="52c13-113">Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="52c13-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="52c13-114">Uma matriz de operadores de medida (cada um sendo uma matriz de Pauli).</span><span class="sxs-lookup"><span data-stu-id="52c13-114">An array of measurement operators (each being an array of Pauli).</span></span>