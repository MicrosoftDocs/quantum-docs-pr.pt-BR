---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliMajIdx_
title: Função _PQTermToPauliMajIdx_
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: edb9302e04de2abc6dfa9da0da27504f776e721f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839297"
---
# <a name="_pqtermtopaulimajidx_-function"></a><span data-ttu-id="ff2c6-102">Função _PQTermToPauliMajIdx_</span><span class="sxs-lookup"><span data-stu-id="ff2c6-102">_PQTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="ff2c6-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="ff2c6-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="ff2c6-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ff2c6-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="ff2c6-105">Converte um GeneratorIndex que descreve um termo PQ para uma expressão ' GeneratorIndex [] ' em termos de Paulis</span><span class="sxs-lookup"><span data-stu-id="ff2c6-105">Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="ff2c6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff2c6-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="ff2c6-107">termo: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ff2c6-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ff2c6-108">`GeneratorIndex` representando um termo de PQ.</span><span class="sxs-lookup"><span data-stu-id="ff2c6-108">`GeneratorIndex` representing a PQ term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="ff2c6-109">Saída: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="ff2c6-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="ff2c6-110">' GeneratorIndex [] ' expressando o termo PQ como termos de Pauli.</span><span class="sxs-lookup"><span data-stu-id="ff2c6-110">'GeneratorIndex[]' expressing PQ term as Pauli terms.</span></span>