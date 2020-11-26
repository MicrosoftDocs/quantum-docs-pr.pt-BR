---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Operação SetToBasisState
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: 2612bfe488c830abd835be89b2f8ea6795abf675
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194144"
---
# <a name="settobasisstate-operation"></a><span data-ttu-id="28c71-102">Operação SetToBasisState</span><span class="sxs-lookup"><span data-stu-id="28c71-102">SetToBasisState operation</span></span>

<span data-ttu-id="28c71-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="28c71-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="28c71-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="28c71-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="28c71-105">Define um qubit para um determinado estado de base computacional medindo o qubit e aplicando uma inversão de bit, se necessário.</span><span class="sxs-lookup"><span data-stu-id="28c71-105">Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.</span></span>

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="28c71-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="28c71-106">Input</span></span>

### <a name="desired--__invalidresult__"></a><span data-ttu-id="28c71-107">desejado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="28c71-107">desired : __invalid<Result>__</span></span>

<span data-ttu-id="28c71-108">O estado base ao qual o qubit deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="28c71-108">The basis state that the qubit should be set to.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="28c71-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="28c71-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="28c71-110">O qubit cujo estado deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="28c71-110">The qubit whose state is to be set.</span></span>



## <a name="output--unit"></a><span data-ttu-id="28c71-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="28c71-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="28c71-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="28c71-112">Remarks</span></span>

<span data-ttu-id="28c71-113">Como uma constante desta operação, chamar `M(q)` imediatamente após `SetToBasisState(result, q)` será retornado `result` .</span><span class="sxs-lookup"><span data-stu-id="28c71-113">As an invariant of this operation, calling `M(q)` immediately after `SetToBasisState(result, q)` will return `result`.</span></span>