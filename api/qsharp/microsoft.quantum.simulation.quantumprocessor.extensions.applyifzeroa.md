---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroA
title: Operação ApplyIfZeroA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroA
qsharp.summary: ''
ms.openlocfilehash: 124c5bbabc9e22804734ddbde955312db9655187
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697123"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="8c624-102">Operação ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="8c624-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="8c624-103">Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="8c624-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="8c624-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8c624-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyIfZeroA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="8c624-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="8c624-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="8c624-106">measurementResult: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="8c624-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit-adj"></a><span data-ttu-id="8c624-107">onResultZeroOp: t => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8c624-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="8c624-108">zeroArg: ' t</span><span class="sxs-lookup"><span data-stu-id="8c624-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="8c624-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8c624-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8c624-110">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="8c624-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8c624-111">T'</span><span class="sxs-lookup"><span data-stu-id="8c624-111">'T</span></span>

