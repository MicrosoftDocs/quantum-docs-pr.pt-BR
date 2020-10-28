---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliGenIdx_
title: Função _PQTermToPauliGenIdx_
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 1f9567f327b5afc3054acbf1a615b44a54453004
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693747"
---
# <a name="_pqtermtopauligenidx_-function"></a><span data-ttu-id="17713-102">Função _PQTermToPauliGenIdx_</span><span class="sxs-lookup"><span data-stu-id="17713-102">_PQTermToPauliGenIdx_ function</span></span>

<span data-ttu-id="17713-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="17713-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="17713-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="17713-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="17713-105">Converte um GeneratorIndex que descreve um termo PQ para uma expressão ' GeneratorIndex [] ' em termos de Paulis</span><span class="sxs-lookup"><span data-stu-id="17713-105">Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQTermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="17713-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="17713-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="17713-107">termo: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="17713-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="17713-108">`GeneratorIndex` representando um termo de PQ.</span><span class="sxs-lookup"><span data-stu-id="17713-108">`GeneratorIndex` representing a PQ term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="17713-109">Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="17713-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="17713-110">' GeneratorIndex [] ' expressando o termo PQ como termos de Pauli.</span><span class="sxs-lookup"><span data-stu-id="17713-110">'GeneratorIndex[]' expressing PQ term as Pauli terms.</span></span>