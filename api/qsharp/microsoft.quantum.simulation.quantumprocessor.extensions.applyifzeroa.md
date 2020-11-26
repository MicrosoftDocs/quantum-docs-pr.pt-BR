---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroA
title: Operação ApplyIfZeroA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroA
qsharp.summary: ''
ms.openlocfilehash: d57f07beddc94d11a2143ba5d1fd975760260731
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230864"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="34a5f-102">Operação ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="34a5f-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="34a5f-103">Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="34a5f-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="34a5f-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="34a5f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZeroA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T)) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="34a5f-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="34a5f-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="34a5f-106">measurementResult: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="34a5f-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-adj"></a><span data-ttu-id="34a5f-107">onResultZeroOp: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="34a5f-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="34a5f-108">zeroArg: ' t</span><span class="sxs-lookup"><span data-stu-id="34a5f-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="34a5f-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="34a5f-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="34a5f-110">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="34a5f-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="34a5f-111">T'</span><span class="sxs-lookup"><span data-stu-id="34a5f-111">'T</span></span>

