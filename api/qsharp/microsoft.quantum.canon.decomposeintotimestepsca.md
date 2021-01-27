---
uid: Microsoft.Quantum.Canon.DecomposeIntoTimeStepsCA
title: Função DecomposeIntoTimeStepsCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposeIntoTimeStepsCA
qsharp.summary: >-
  > [!WARNING]

  > DecomposeIntoTimeStepsCA has been deprecated. Please use <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA> instead.
ms.openlocfilehash: aa004098cbc805126109d3356f0f6550b85cd60b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840725"
---
# <a name="decomposeintotimestepsca-function"></a><span data-ttu-id="6d577-102">Função DecomposeIntoTimeStepsCA</span><span class="sxs-lookup"><span data-stu-id="6d577-102">DecomposeIntoTimeStepsCA function</span></span>

<span data-ttu-id="6d577-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6d577-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6d577-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6d577-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="6d577-105">DecomposeIntoTimeStepsCA foi preterido.</span><span class="sxs-lookup"><span data-stu-id="6d577-105">DecomposeIntoTimeStepsCA has been deprecated.</span></span> <span data-ttu-id="6d577-106">Use <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="6d577-106">Please use <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA> instead.</span></span>



```qsharp
function DecomposeIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="6d577-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d577-107">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="6d577-108">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6d577-108">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="6d577-109">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="6d577-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="trotterorder--int"></a><span data-ttu-id="6d577-110">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6d577-110">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--doublet--unit--is-adj--ctl"></a><span data-ttu-id="6d577-111">Saída: ([Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="6d577-111">Output : ([Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6d577-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="6d577-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6d577-113">T'</span><span class="sxs-lookup"><span data-stu-id="6d577-113">'T</span></span>

