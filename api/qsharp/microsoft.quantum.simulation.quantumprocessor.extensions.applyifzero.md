---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZero
title: Operação ApplyIfZero
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZero
qsharp.summary: ''
ms.openlocfilehash: 867e2e78ea787c2376fb2b1dcc6c72694fe08621
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230898"
---
# <a name="applyifzero-operation"></a><span data-ttu-id="7cf3b-102">Operação ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="7cf3b-102">ApplyIfZero operation</span></span>

<span data-ttu-id="7cf3b-103">Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="7cf3b-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="7cf3b-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7cf3b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZero<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="7cf3b-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="7cf3b-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="7cf3b-106">measurementResult: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="7cf3b-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit"></a><span data-ttu-id="7cf3b-107">onResultZeroOp: t = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="7cf3b-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="zeroarg--t"></a><span data-ttu-id="7cf3b-108">zeroArg: ' t</span><span class="sxs-lookup"><span data-stu-id="7cf3b-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="7cf3b-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7cf3b-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7cf3b-110">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="7cf3b-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7cf3b-111">T'</span><span class="sxs-lookup"><span data-stu-id="7cf3b-111">'T</span></span>

