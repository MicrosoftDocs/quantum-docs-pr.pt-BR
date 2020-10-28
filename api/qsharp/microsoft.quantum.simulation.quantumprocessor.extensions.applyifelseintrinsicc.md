---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseIntrinsicC
title: Operação ApplyIfElseIntrinsicC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseIntrinsicC
qsharp.summary: ''
ms.openlocfilehash: 178d4b704d84090f1f8592b857c3da659e5c50bb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696992"
---
# <a name="applyifelseintrinsicc-operation"></a><span data-ttu-id="7e3a4-102">Operação ApplyIfElseIntrinsicC</span><span class="sxs-lookup"><span data-stu-id="7e3a4-102">ApplyIfElseIntrinsicC operation</span></span>

<span data-ttu-id="7e3a4-103">Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="7e3a4-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="7e3a4-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7e3a4-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfElseIntrinsicC (measurementResult : Result, onResultZeroOp : (Unit => Unit is Ctl), onResultOneOp : (Unit => Unit is Ctl)) : Unit
```


## <a name="input"></a><span data-ttu-id="7e3a4-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e3a4-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="7e3a4-106">measurementResult: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="7e3a4-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--unit--unit-ctl"></a><span data-ttu-id="7e3a4-107">onResultZeroOp: [Unit](xref:microsoft.quantum.lang-ref.unit) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) de unidade</span><span class="sxs-lookup"><span data-stu-id="7e3a4-107">onResultZeroOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="onresultoneop--unit--unit-ctl"></a><span data-ttu-id="7e3a4-108">onResultOneOp: [Unit](xref:microsoft.quantum.lang-ref.unit) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) de unidade</span><span class="sxs-lookup"><span data-stu-id="7e3a4-108">onResultOneOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>





## <a name="output--unit"></a><span data-ttu-id="7e3a4-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7e3a4-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

