---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQandPQQRTermToPauliMajIdx_
title: Função _PQandPQQRTermToPauliMajIdx_
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQandPQQRTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 68a9aec7768269e2d5f295d5ea3cbb136ea1ef2c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851490"
---
# <a name="_pqandpqqrtermtopaulimajidx_-function"></a><span data-ttu-id="7233c-102">Função _PQandPQQRTermToPauliMajIdx_</span><span class="sxs-lookup"><span data-stu-id="7233c-102">_PQandPQQRTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="7233c-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="7233c-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="7233c-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="7233c-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="7233c-105">Converte um GeneratorIndex que descreve um termo PQ ou PQQR para uma expressão ' GeneratorIndex [] ' em termos de Paulis</span><span class="sxs-lookup"><span data-stu-id="7233c-105">Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQandPQQRTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="7233c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7233c-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="7233c-107">termo: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="7233c-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="7233c-108">`GeneratorIndex` representando um termo PQ ou PQQR.</span><span class="sxs-lookup"><span data-stu-id="7233c-108">`GeneratorIndex` representing a PQ or PQQR term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="7233c-109">Saída: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="7233c-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="7233c-110">' GeneratorIndex [] ' expressando o termo PQ ou PQQR como termos de Pauli.</span><span class="sxs-lookup"><span data-stu-id="7233c-110">'GeneratorIndex[]' expressing PQ or PQQR term as Pauli terms.</span></span>