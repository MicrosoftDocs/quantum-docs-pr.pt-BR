---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: Função HTermsToGenIdx
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 73324a48cc4b42de0d5d8618ad9e833d289125f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693820"
---
# <a name="htermstogenidx-function"></a><span data-ttu-id="6ef59-102">Função HTermsToGenIdx</span><span class="sxs-lookup"><span data-stu-id="6ef59-102">HTermsToGenIdx function</span></span>

<span data-ttu-id="6ef59-103">Namespace: [Microsoft. Quantum. química](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="6ef59-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="6ef59-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6ef59-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6ef59-105">Converte um índice em um termo Hamiltonian no `HTerm[]` formato de dados em um GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="6ef59-105">Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="6ef59-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6ef59-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="6ef59-107">dados: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="6ef59-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="6ef59-108">Dados de entrada no `HTerm[]` formato.</span><span class="sxs-lookup"><span data-stu-id="6ef59-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="6ef59-109">termtype: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6ef59-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="6ef59-110">Informações adicionais adicionadas ao GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="6ef59-110">Additional information added to GeneratorIndex.</span></span>


### <a name="idx--int"></a><span data-ttu-id="6ef59-111">IDX: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6ef59-111">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6ef59-112">Indexar em um termo de Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="6ef59-112">Index to a term of the Hamiltonian</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="6ef59-113">Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="6ef59-113">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="6ef59-114">Um GeneratorIndex que representa um termo Hamiltonian representado pelo `data[idx]` , junto com informações adicionais adicionadas pelo `termType` .</span><span class="sxs-lookup"><span data-stu-id="6ef59-114">A GeneratorIndex representing a Hamiltonian term represented by `data[idx]`, together with additional information added by `termType`.</span></span>