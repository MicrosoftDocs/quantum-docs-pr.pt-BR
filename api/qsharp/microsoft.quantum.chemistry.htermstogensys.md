---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: Função HTermsToGenSys
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: b78ff393fa1e51c38028ef56bb3c61b8f1d5e478
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693818"
---
# <a name="htermstogensys-function"></a><span data-ttu-id="9a3fa-102">Função HTermsToGenSys</span><span class="sxs-lookup"><span data-stu-id="9a3fa-102">HTermsToGenSys function</span></span>

<span data-ttu-id="9a3fa-103">Namespace: [Microsoft. Quantum. química](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="9a3fa-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="9a3fa-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9a3fa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9a3fa-105">Converte um Hamiltonian no `HTerm[]` formato de dados em um GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="9a3fa-105">Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.</span></span>

```qsharp
function HTermsToGenSys (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="9a3fa-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a3fa-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="9a3fa-107">dados: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="9a3fa-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="9a3fa-108">Dados de entrada no `HTerm[]` formato.</span><span class="sxs-lookup"><span data-stu-id="9a3fa-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="9a3fa-109">termtype: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="9a3fa-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="9a3fa-110">Informações adicionais adicionadas ao GeneratorIndex.</span><span class="sxs-lookup"><span data-stu-id="9a3fa-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="9a3fa-111">Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="9a3fa-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="9a3fa-112">Um GeneratorSystem que representa um Hamiltonian representado pela entrada `data` .</span><span class="sxs-lookup"><span data-stu-id="9a3fa-112">A GeneratorSystem representing a Hamiltonian represented by the input `data`.</span></span>