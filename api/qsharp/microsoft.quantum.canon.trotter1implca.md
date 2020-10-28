---
uid: Microsoft.Quantum.Canon.Trotter1ImplCA
title: Operação Trotter1ImplCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter1ImplCA
qsharp.summary: Implementation of the first-order Trotter–Suzuki integrator.
ms.openlocfilehash: 250b80729530a5d3054e037d9dd653904a57f6d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693884"
---
# <a name="trotter1implca-operation"></a><span data-ttu-id="3625f-102">Operação Trotter1ImplCA</span><span class="sxs-lookup"><span data-stu-id="3625f-102">Trotter1ImplCA operation</span></span>

<span data-ttu-id="3625f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3625f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3625f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3625f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3625f-105">Implementação da primeira ordem Trotter – integrador Suzuki.</span><span class="sxs-lookup"><span data-stu-id="3625f-105">Implementation of the first-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter1ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="3625f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="3625f-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="3625f-107">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3625f-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3625f-108">O número de operações a serem decompostas em etapas de tempo.</span><span class="sxs-lookup"><span data-stu-id="3625f-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit-adj--ctl"></a><span data-ttu-id="3625f-109">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="3625f-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="3625f-110">Uma operação que aceita uma entrada de índice (tipo `Int` ) e uma entrada de hora (tipo `Double` ) e um registro Quantum (tipo `'T` ) para decomposição.</span><span class="sxs-lookup"><span data-stu-id="3625f-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="3625f-111">Etapas: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3625f-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3625f-112">Multiplicador no tamanho de cada etapa da simulação.</span><span class="sxs-lookup"><span data-stu-id="3625f-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="3625f-113">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="3625f-113">target : 'T</span></span>

<span data-ttu-id="3625f-114">Um registro Quantum no qual as operações agem.</span><span class="sxs-lookup"><span data-stu-id="3625f-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3625f-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3625f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3625f-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="3625f-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3625f-117">T'</span><span class="sxs-lookup"><span data-stu-id="3625f-117">'T</span></span>

<span data-ttu-id="3625f-118">O tipo em que cada etapa de tempo deve agir; Normalmente, o `Qubit[]` ou o `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="3625f-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>