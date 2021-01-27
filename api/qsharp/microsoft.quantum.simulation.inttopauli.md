---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: Função IntToPauli
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: 76f482b86ff4a27b6e6ce6ae4ec3d59422563f12
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842246"
---
# <a name="inttopauli-function"></a><span data-ttu-id="8ada1-102">Função IntToPauli</span><span class="sxs-lookup"><span data-stu-id="8ada1-102">IntToPauli function</span></span>

<span data-ttu-id="8ada1-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="8ada1-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="8ada1-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8ada1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8ada1-105">Converte um inteiro em um operador qubit Pauli único.</span><span class="sxs-lookup"><span data-stu-id="8ada1-105">Converts a integer to a single-qubit Pauli operator.</span></span>

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a><span data-ttu-id="8ada1-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8ada1-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="8ada1-107">IDX: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8ada1-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8ada1-108">Número inteiro no intervalo `0..3` a ser convertido em operadores Pauli.</span><span class="sxs-lookup"><span data-stu-id="8ada1-108">Integer in the range `0..3` to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="8ada1-109">Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="8ada1-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="8ada1-110">Um `Pauli` operador fornecido por `[PauliI, PauliX, PauliY, PauliZ][idx]` .</span><span class="sxs-lookup"><span data-stu-id="8ada1-110">A `Pauli` operator given by `[PauliI, PauliX, PauliY, PauliZ][idx]`.</span></span>