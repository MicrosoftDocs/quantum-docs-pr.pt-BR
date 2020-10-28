---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: Operação TrotterArbitraryImplCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: 1c094d09ac8bdd71a59ef57d8715a6f90f18efc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693882"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="91a8a-102">Operação TrotterArbitraryImplCA</span><span class="sxs-lookup"><span data-stu-id="91a8a-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="91a8a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="91a8a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="91a8a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="91a8a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="91a8a-105">Implementação recursiva de Trotter de ordem par – integrador de Suzuki.</span><span class="sxs-lookup"><span data-stu-id="91a8a-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="91a8a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="91a8a-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="91a8a-107">ordem: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="91a8a-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="91a8a-108">Ordem do integrador Trotter-Suzuki.</span><span class="sxs-lookup"><span data-stu-id="91a8a-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="91a8a-109">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="91a8a-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="91a8a-110">O número de operações a serem decompostas em etapas de tempo.</span><span class="sxs-lookup"><span data-stu-id="91a8a-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit-adj--ctl"></a><span data-ttu-id="91a8a-111">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="91a8a-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="91a8a-112">Uma operação que aceita uma entrada de índice (tipo `Int` ) e uma entrada de hora (tipo `Double` ) e um registro Quantum (tipo `'T` ) para decomposição.</span><span class="sxs-lookup"><span data-stu-id="91a8a-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="91a8a-113">Etapas: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="91a8a-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="91a8a-114">Multiplicador no tamanho de cada etapa da simulação.</span><span class="sxs-lookup"><span data-stu-id="91a8a-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="91a8a-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="91a8a-115">target : 'T</span></span>

<span data-ttu-id="91a8a-116">Um registro Quantum no qual as operações agem.</span><span class="sxs-lookup"><span data-stu-id="91a8a-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="91a8a-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="91a8a-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="91a8a-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="91a8a-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="91a8a-119">T'</span><span class="sxs-lookup"><span data-stu-id="91a8a-119">'T</span></span>

<span data-ttu-id="91a8a-120">O tipo em que cada etapa de tempo deve agir; Normalmente, o `Qubit[]` ou o `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="91a8a-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>