---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRCA
title: Operação ApplyIfElseRCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRCA
qsharp.summary: ''
ms.openlocfilehash: 6fbf186575775b3ae18a41727c225fb871f8dac0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192614"
---
# <a name="applyifelserca-operation"></a><span data-ttu-id="dec76-102">Operação ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="dec76-102">ApplyIfElseRCA operation</span></span>

<span data-ttu-id="dec76-103">Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="dec76-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="dec76-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="dec76-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfElseRCA<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj + Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Adj + Ctl), oneArg : 'U)) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="dec76-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="dec76-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="dec76-106">measurementResult: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="dec76-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-adj--ctl"></a><span data-ttu-id="dec76-107">onResultZeroOp: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="dec76-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="dec76-108">zeroArg: ' t</span><span class="sxs-lookup"><span data-stu-id="dec76-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit--is-adj--ctl"></a><span data-ttu-id="dec76-109">onResultOneOp: ' U => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="dec76-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="onearg--u"></a><span data-ttu-id="dec76-110">oneArg: ' U</span><span class="sxs-lookup"><span data-stu-id="dec76-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="dec76-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dec76-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dec76-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="dec76-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dec76-113">T'</span><span class="sxs-lookup"><span data-stu-id="dec76-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="dec76-114">' U</span><span class="sxs-lookup"><span data-stu-id="dec76-114">'U</span></span>

