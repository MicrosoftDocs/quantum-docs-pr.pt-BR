---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: Função PauliStringFromGenIdx
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: a937dc648c5de5a5f6de7da996448af497b92185
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230303"
---
# <a name="paulistringfromgenidx-function"></a><span data-ttu-id="ab45b-102">Função PauliStringFromGenIdx</span><span class="sxs-lookup"><span data-stu-id="ab45b-102">PauliStringFromGenIdx function</span></span>

<span data-ttu-id="ab45b-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ab45b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ab45b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ab45b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ab45b-105">Extrai a cadeia de caracteres Pauli e seus índices qubit de um termo Pauli descrito por um `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="ab45b-105">Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a><span data-ttu-id="ab45b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab45b-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="ab45b-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ab45b-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ab45b-108">`GeneratorIndex` tipo que codifica um termo de Pauli.</span><span class="sxs-lookup"><span data-stu-id="ab45b-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--pauliint"></a><span data-ttu-id="ab45b-109">Saída: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="ab45b-109">Output : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

<span data-ttu-id="ab45b-110">A cadeia de caracteres Pauli do termo descrito por um `GeneratorIndex` e os índices para o qubits em que ele atua.</span><span class="sxs-lookup"><span data-stu-id="ab45b-110">The Pauli string of the term described by a `GeneratorIndex`, and indices to the qubits it acts on.</span></span>