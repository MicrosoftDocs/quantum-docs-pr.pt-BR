---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyIntrinsicCA
title: Operação ApplyConditionallyIntrinsicCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyIntrinsicCA
qsharp.summary: ''
ms.openlocfilehash: 7cdddba45824d5e5037270d8578f2cb16c03be83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694620"
---
# <a name="applyconditionallyintrinsicca-operation"></a><span data-ttu-id="e70b3-102">Operação ApplyConditionallyIntrinsicCA</span><span class="sxs-lookup"><span data-stu-id="e70b3-102">ApplyConditionallyIntrinsicCA operation</span></span>

<span data-ttu-id="e70b3-103">Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="e70b3-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="e70b3-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e70b3-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyConditionallyIntrinsicCA (measurementResults : Result[], resultsValues : Result[], onEqualOp : (Unit => Unit is Ctl + Adj), onNonEqualOp : (Unit => Unit is Ctl + Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="e70b3-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="e70b3-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="e70b3-106">measurementResults: __inválido <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="e70b3-106">measurementResults : __invalid<Result>__ []</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="e70b3-107">resultsValues: __inválido <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="e70b3-107">resultsValues : __invalid<Result>__ []</span></span>




### <a name="onequalop--unit--unit-ctl--adj"></a><span data-ttu-id="e70b3-108">onEqualOp: [unidade](xref:microsoft.quantum.lang-ref.unit) de => [Unit](xref:microsoft.quantum.lang-ref.unit) lista de certificados confiáveis + adj</span><span class="sxs-lookup"><span data-stu-id="e70b3-108">onEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>




### <a name="onnonequalop--unit--unit-ctl--adj"></a><span data-ttu-id="e70b3-109">onNonEqualOp: [unidade](xref:microsoft.quantum.lang-ref.unit) de => [Unit](xref:microsoft.quantum.lang-ref.unit) lista de certificados confiáveis + adj</span><span class="sxs-lookup"><span data-stu-id="e70b3-109">onNonEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>





## <a name="output--unit"></a><span data-ttu-id="e70b3-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e70b3-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

