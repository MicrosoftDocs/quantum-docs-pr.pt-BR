---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: Função HTermsToGenIdx
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 84dc132528f8fd1c45fb2f7345111a05626ee686
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839624"
---
# <a name="htermstogenidx-function"></a><span data-ttu-id="d4e71-102">Função HTermsToGenIdx</span><span class="sxs-lookup"><span data-stu-id="d4e71-102">HTermsToGenIdx function</span></span>

<span data-ttu-id="d4e71-103">Namespace: [Microsoft. Quantum. química](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d4e71-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="d4e71-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d4e71-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="d4e71-105">Converte um índice em um termo Hamiltonian no `HTerm[]` formato de dados em um GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="d4e71-105">Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="d4e71-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d4e71-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="d4e71-107">dados: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="d4e71-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="d4e71-108">Dados de entrada no `HTerm[]` formato.</span><span class="sxs-lookup"><span data-stu-id="d4e71-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="d4e71-109">termtype: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d4e71-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d4e71-110">Informações adicionais adicionadas ao GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="d4e71-110">Additional information added to GeneratorIndex.</span></span>


### <a name="idx--int"></a><span data-ttu-id="d4e71-111">IDX: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d4e71-111">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d4e71-112">Indexar em um termo de Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="d4e71-112">Index to a term of the Hamiltonian</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="d4e71-113">Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="d4e71-113">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="d4e71-114">Um GeneratorIndex que representa um termo Hamiltonian representado pelo `data[idx]` , junto com informações adicionais adicionadas pelo `termType` .</span><span class="sxs-lookup"><span data-stu-id="d4e71-114">A GeneratorIndex representing a Hamiltonian term represented by `data[idx]`, together with additional information added by `termType`.</span></span>