---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyIntrinsic
title: Operação ApplyConditionallyIntrinsic
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyIntrinsic
qsharp.summary: ''
ms.openlocfilehash: 2301ef25a262ead63c3550777af79e1d3f9c5a98
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858483"
---
# <a name="applyconditionallyintrinsic-operation"></a><span data-ttu-id="7eec8-102">Operação ApplyConditionallyIntrinsic</span><span class="sxs-lookup"><span data-stu-id="7eec8-102">ApplyConditionallyIntrinsic operation</span></span>

<span data-ttu-id="7eec8-103">Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="7eec8-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="7eec8-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7eec8-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyConditionallyIntrinsic (measurementResults : Result[], resultsValues : Result[], onEqualOp : (Unit => Unit), onNonEqualOp : (Unit => Unit)) : Unit
```


## <a name="input"></a><span data-ttu-id="7eec8-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="7eec8-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="7eec8-106">measurementResults: __inválido <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="7eec8-106">measurementResults : __invalid<Result>__[]</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="7eec8-107">resultsValues: __inválido <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="7eec8-107">resultsValues : __invalid<Result>__[]</span></span>




### <a name="onequalop--unit--unit"></a><span data-ttu-id="7eec8-108">onEqualOp: [](xref:microsoft.quantum.lang-ref.unit) => [unidade](xref:microsoft.quantum.lang-ref.unit) de unidade</span><span class="sxs-lookup"><span data-stu-id="7eec8-108">onEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="onnonequalop--unit--unit"></a><span data-ttu-id="7eec8-109">onNonEqualOp: [](xref:microsoft.quantum.lang-ref.unit) => [unidade](xref:microsoft.quantum.lang-ref.unit) de unidade</span><span class="sxs-lookup"><span data-stu-id="7eec8-109">onNonEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 





## <a name="output--unit"></a><span data-ttu-id="7eec8-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7eec8-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

