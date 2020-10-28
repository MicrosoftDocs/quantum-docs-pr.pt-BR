---
uid: Microsoft.Quantum.Canon.DecomposeIntoTimeStepsCA
title: Função DecomposeIntoTimeStepsCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposeIntoTimeStepsCA
qsharp.summary: >-
  > [!WARNING]

  > DecomposeIntoTimeStepsCA has been deprecated. Please use <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA> instead.
ms.openlocfilehash: b6f3fe0ececc58d86b916841c513377fbcb59054
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694031"
---
# <a name="decomposeintotimestepsca-function"></a><span data-ttu-id="91fb2-102">Função DecomposeIntoTimeStepsCA</span><span class="sxs-lookup"><span data-stu-id="91fb2-102">DecomposeIntoTimeStepsCA function</span></span>

<span data-ttu-id="91fb2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="91fb2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="91fb2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="91fb2-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="91fb2-105">DecomposeIntoTimeStepsCA foi preterido.</span><span class="sxs-lookup"><span data-stu-id="91fb2-105">DecomposeIntoTimeStepsCA has been deprecated.</span></span> <span data-ttu-id="91fb2-106">Use <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="91fb2-106">Please use <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA> instead.</span></span>



```qsharp
function DecomposeIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="91fb2-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="91fb2-107">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="91fb2-108">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="91fb2-108">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="op--intdoublet--unit-adj--ctl"></a><span data-ttu-id="91fb2-109">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="91fb2-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="trotterorder--int"></a><span data-ttu-id="91fb2-110">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="91fb2-110">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--doublet--unit-adj--ctl"></a><span data-ttu-id="91fb2-111">Saída: ([Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit) adj + CTL</span><span class="sxs-lookup"><span data-stu-id="91fb2-111">Output : ([Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="type-parameters"></a><span data-ttu-id="91fb2-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="91fb2-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="91fb2-113">T'</span><span class="sxs-lookup"><span data-stu-id="91fb2-113">'T</span></span>

