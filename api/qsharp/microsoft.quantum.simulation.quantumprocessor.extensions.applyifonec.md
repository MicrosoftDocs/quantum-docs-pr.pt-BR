---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOneC
title: Operação ApplyIfOneC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOneC
qsharp.summary: ''
ms.openlocfilehash: ae6e0d16424e745303b377e70927cda847d2f1e8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858730"
---
# <a name="applyifonec-operation"></a><span data-ttu-id="d128d-102">Operação ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="d128d-102">ApplyIfOneC operation</span></span>

<span data-ttu-id="d128d-103">Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="d128d-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="d128d-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d128d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfOneC<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit is Ctl), oneArg : 'T)) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="d128d-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="d128d-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="d128d-106">measurementResult: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="d128d-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit--is-ctl"></a><span data-ttu-id="d128d-107">onResultOneOp: T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="d128d-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="onearg--t"></a><span data-ttu-id="d128d-108">oneArg: ' t</span><span class="sxs-lookup"><span data-stu-id="d128d-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="d128d-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d128d-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d128d-110">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d128d-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d128d-111">T'</span><span class="sxs-lookup"><span data-stu-id="d128d-111">'T</span></span>

