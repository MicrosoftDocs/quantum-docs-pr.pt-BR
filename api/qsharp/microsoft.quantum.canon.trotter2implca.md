---
uid: Microsoft.Quantum.Canon.Trotter2ImplCA
title: Operação Trotter2ImplCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter2ImplCA
qsharp.summary: Implementation of the second-order Trotter–Suzuki integrator.
ms.openlocfilehash: 34b60934b67c19b2d1d718d68b85a2f0fffeab5d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852027"
---
# <a name="trotter2implca-operation"></a><span data-ttu-id="1f1bb-102">Operação Trotter2ImplCA</span><span class="sxs-lookup"><span data-stu-id="1f1bb-102">Trotter2ImplCA operation</span></span>

<span data-ttu-id="1f1bb-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1f1bb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1f1bb-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1f1bb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1f1bb-105">Implementação da segunda ordem Trotter – integrador Suzuki.</span><span class="sxs-lookup"><span data-stu-id="1f1bb-105">Implementation of the second-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter2ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1f1bb-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f1bb-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="1f1bb-107">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1f1bb-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1f1bb-108">O número de operações a serem decompostas em etapas de tempo.</span><span class="sxs-lookup"><span data-stu-id="1f1bb-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="1f1bb-109">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="1f1bb-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1f1bb-110">Uma operação que aceita uma entrada de índice (tipo `Int` ) e uma entrada de hora (tipo `Double` ) e um registro Quantum (tipo `'T` ) para decomposição.</span><span class="sxs-lookup"><span data-stu-id="1f1bb-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="1f1bb-111">Etapas: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1f1bb-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1f1bb-112">Multiplicador no tamanho de cada etapa da simulação.</span><span class="sxs-lookup"><span data-stu-id="1f1bb-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="1f1bb-113">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="1f1bb-113">target : 'T</span></span>

<span data-ttu-id="1f1bb-114">Um registro Quantum no qual as operações agem.</span><span class="sxs-lookup"><span data-stu-id="1f1bb-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1f1bb-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1f1bb-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1f1bb-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="1f1bb-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1f1bb-117">T'</span><span class="sxs-lookup"><span data-stu-id="1f1bb-117">'T</span></span>

<span data-ttu-id="1f1bb-118">O tipo em que cada etapa de tempo deve agir; Normalmente, o `Qubit[]` ou o `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="1f1bb-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="example"></a><span data-ttu-id="1f1bb-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1f1bb-119">Example</span></span>

<span data-ttu-id="1f1bb-120">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="1f1bb-120">The following are equivalent:</span></span>

```qsharp
op(0, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(0, deltaT / 2.0, target);
```

<span data-ttu-id="1f1bb-121">e</span><span class="sxs-lookup"><span data-stu-id="1f1bb-121">and</span></span>

```qsharp
Trotter2ImplCA((2, op), deltaT, target);
```