---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: Função HTermToGenIdx
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: dd72355adb32f9a0d109ee36b24be2d445f3fa66
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693817"
---
# <a name="htermtogenidx-function"></a><span data-ttu-id="b292a-102">Função HTermToGenIdx</span><span class="sxs-lookup"><span data-stu-id="b292a-102">HTermToGenIdx function</span></span>

<span data-ttu-id="b292a-103">Namespace: [Microsoft. Quantum. química](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="b292a-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="b292a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b292a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b292a-105">Converte um termo Hamiltonian no `HTerm` formato de dados em um GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="b292a-105">Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="b292a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b292a-106">Input</span></span>

### <a name="term--hterm"></a><span data-ttu-id="b292a-107">termo: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)</span><span class="sxs-lookup"><span data-stu-id="b292a-107">term : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)</span></span>

<span data-ttu-id="b292a-108">Dados de entrada no `HTerm` formato.</span><span class="sxs-lookup"><span data-stu-id="b292a-108">Input data in `HTerm` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="b292a-109">termtype: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b292a-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b292a-110">Informações adicionais adicionadas ao GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="b292a-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="b292a-111">Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="b292a-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="b292a-112">Um GeneratorIndex que representa um termo Hamiltonian representado pelo `term` , junto com informações adicionais adicionadas pelo `termType` .</span><span class="sxs-lookup"><span data-stu-id="b292a-112">A GeneratorIndex representing a Hamiltonian term represented by `term`, together with additional information added by `termType`.</span></span>