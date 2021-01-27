---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Operação SetToBasisState
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: dfa054360a5e82b7ae6ec5a6d52e7d5fe566f42e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854620"
---
# <a name="settobasisstate-operation"></a><span data-ttu-id="b09de-102">Operação SetToBasisState</span><span class="sxs-lookup"><span data-stu-id="b09de-102">SetToBasisState operation</span></span>

<span data-ttu-id="b09de-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="b09de-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="b09de-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b09de-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b09de-105">Define um qubit para um determinado estado de base computacional medindo o qubit e aplicando uma inversão de bit, se necessário.</span><span class="sxs-lookup"><span data-stu-id="b09de-105">Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.</span></span>

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="b09de-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b09de-106">Input</span></span>

### <a name="desired--__invalidresult__"></a><span data-ttu-id="b09de-107">desejado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="b09de-107">desired : __invalid<Result>__</span></span>

<span data-ttu-id="b09de-108">O estado base ao qual o qubit deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="b09de-108">The basis state that the qubit should be set to.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="b09de-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b09de-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b09de-110">O qubit cujo estado deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="b09de-110">The qubit whose state is to be set.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b09de-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b09de-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b09de-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b09de-112">Remarks</span></span>

<span data-ttu-id="b09de-113">Como uma constante desta operação, chamar `M(q)` imediatamente após `SetToBasisState(result, q)` será retornado `result` .</span><span class="sxs-lookup"><span data-stu-id="b09de-113">As an invariant of this operation, calling `M(q)` immediately after `SetToBasisState(result, q)` will return `result`.</span></span>