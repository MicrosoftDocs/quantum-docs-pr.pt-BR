---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Operação ApplyBlockEncodingByLCU
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 1575b93b6c3242e1dffafb330c44cc017a72a8b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694942"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="aed8d-102">Operação ApplyBlockEncodingByLCU</span><span class="sxs-lookup"><span data-stu-id="aed8d-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="aed8d-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="aed8d-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="aed8d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aed8d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aed8d-105">Implementação de `BlockEncodingByLCU`.</span><span class="sxs-lookup"><span data-stu-id="aed8d-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit
```


## <a name="input"></a><span data-ttu-id="aed8d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="aed8d-106">Input</span></span>

### <a name="statepreparation--t--unit-adj--ctl"></a><span data-ttu-id="aed8d-107">statePreparation: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="aed8d-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="selector--ts--unit-adj--ctl"></a><span data-ttu-id="aed8d-108">seletor: (t, ' s) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="aed8d-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="aed8d-109">auxiliares: ' t</span><span class="sxs-lookup"><span data-stu-id="aed8d-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="aed8d-110">sistema: ' s</span><span class="sxs-lookup"><span data-stu-id="aed8d-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="aed8d-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aed8d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="aed8d-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="aed8d-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aed8d-113">T'</span><span class="sxs-lookup"><span data-stu-id="aed8d-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="aed8d-114">Do</span><span class="sxs-lookup"><span data-stu-id="aed8d-114">'S</span></span>

