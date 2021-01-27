---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: Operação TrotterArbitraryImplCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: bb93517a479ce344277bfe97d070e6630a8fccc0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840091"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="a8d4d-102">Operação TrotterArbitraryImplCA</span><span class="sxs-lookup"><span data-stu-id="a8d4d-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="a8d4d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a8d4d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a8d4d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a8d4d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a8d4d-105">Implementação recursiva de Trotter de ordem par – integrador de Suzuki.</span><span class="sxs-lookup"><span data-stu-id="a8d4d-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a8d4d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a8d4d-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="a8d4d-107">ordem: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a8d4d-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a8d4d-108">Ordem do integrador Trotter-Suzuki.</span><span class="sxs-lookup"><span data-stu-id="a8d4d-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="a8d4d-109">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a8d4d-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a8d4d-110">O número de operações a serem decompostas em etapas de tempo.</span><span class="sxs-lookup"><span data-stu-id="a8d4d-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="a8d4d-111">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="a8d4d-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a8d4d-112">Uma operação que aceita uma entrada de índice (tipo `Int` ) e uma entrada de hora (tipo `Double` ) e um registro Quantum (tipo `'T` ) para decomposição.</span><span class="sxs-lookup"><span data-stu-id="a8d4d-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="a8d4d-113">Etapas: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a8d4d-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a8d4d-114">Multiplicador no tamanho de cada etapa da simulação.</span><span class="sxs-lookup"><span data-stu-id="a8d4d-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="a8d4d-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="a8d4d-115">target : 'T</span></span>

<span data-ttu-id="a8d4d-116">Um registro Quantum no qual as operações agem.</span><span class="sxs-lookup"><span data-stu-id="a8d4d-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a8d4d-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a8d4d-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a8d4d-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a8d4d-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a8d4d-119">T'</span><span class="sxs-lookup"><span data-stu-id="a8d4d-119">'T</span></span>

<span data-ttu-id="a8d4d-120">O tipo em que cada etapa de tempo deve agir; Normalmente, o `Qubit[]` ou o `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="a8d4d-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>