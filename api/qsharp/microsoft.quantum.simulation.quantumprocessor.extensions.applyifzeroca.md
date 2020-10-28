---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroCA
title: Operação ApplyIfZeroCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroCA
qsharp.summary: ''
ms.openlocfilehash: 978964888a89ca46847ae7aa01a2c180ee322436
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697119"
---
# <a name="applyifzeroca-operation"></a><span data-ttu-id="b4040-102">Operação ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="b4040-102">ApplyIfZeroCA operation</span></span>

<span data-ttu-id="b4040-103">Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="b4040-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="b4040-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b4040-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfZeroCA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl + Adj), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="b4040-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="b4040-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="b4040-106">measurementResult: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="b4040-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-ctl--adj"></a><span data-ttu-id="b4040-107">onResultZeroOp: t => da [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj</span><span class="sxs-lookup"><span data-stu-id="b4040-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="b4040-108">zeroArg: ' t</span><span class="sxs-lookup"><span data-stu-id="b4040-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="b4040-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b4040-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b4040-110">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b4040-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b4040-111">T'</span><span class="sxs-lookup"><span data-stu-id="b4040-111">'T</span></span>

