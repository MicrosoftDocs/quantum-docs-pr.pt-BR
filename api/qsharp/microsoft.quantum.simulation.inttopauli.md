---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: Função IntToPauli
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: f0f1186f14a0dc30bb34bd29f148cdc830fd1337
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697001"
---
# <a name="inttopauli-function"></a><span data-ttu-id="ee76a-102">Função IntToPauli</span><span class="sxs-lookup"><span data-stu-id="ee76a-102">IntToPauli function</span></span>

<span data-ttu-id="ee76a-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ee76a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ee76a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ee76a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ee76a-105">Converte um inteiro em um operador qubit Pauli único.</span><span class="sxs-lookup"><span data-stu-id="ee76a-105">Converts a integer to a single-qubit Pauli operator.</span></span>

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a><span data-ttu-id="ee76a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee76a-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="ee76a-107">IDX: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ee76a-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ee76a-108">Número inteiro no intervalo `0..3` a ser convertido em operadores Pauli.</span><span class="sxs-lookup"><span data-stu-id="ee76a-108">Integer in the range `0..3` to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="ee76a-109">Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="ee76a-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="ee76a-110">Um `Pauli` operador fornecido por `[PauliI, PauliX, PauliY, PauliZ][idx]` .</span><span class="sxs-lookup"><span data-stu-id="ee76a-110">A `Pauli` operator given by `[PauliI, PauliX, PauliY, PauliZ][idx]`.</span></span>