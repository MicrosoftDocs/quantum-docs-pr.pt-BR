---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroCA
title: Operação ApplyIfZeroCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroCA
qsharp.summary: ''
ms.openlocfilehash: accc3ca9c0d99c48c713333ce1cc907054c2a860
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230779"
---
# <a name="applyifzeroca-operation"></a><span data-ttu-id="d1a17-102">Operação ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="d1a17-102">ApplyIfZeroCA operation</span></span>

<span data-ttu-id="d1a17-103">Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="d1a17-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="d1a17-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d1a17-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZeroCA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl + Adj), zeroArg : 'T)) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d1a17-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1a17-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="d1a17-106">measurementResult: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="d1a17-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-adj--ctl"></a><span data-ttu-id="d1a17-107">onResultZeroOp: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="d1a17-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="d1a17-108">zeroArg: ' t</span><span class="sxs-lookup"><span data-stu-id="d1a17-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="d1a17-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d1a17-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d1a17-110">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d1a17-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d1a17-111">T'</span><span class="sxs-lookup"><span data-stu-id="d1a17-111">'T</span></span>

