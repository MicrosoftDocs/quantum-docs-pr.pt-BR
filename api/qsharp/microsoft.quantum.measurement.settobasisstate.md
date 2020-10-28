---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Operação SetToBasisState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: bb40ddcf6518a30f5d88eec21cf8e2c2d6e0bbaf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696976"
---
# <a name="settobasisstate-operation"></a><span data-ttu-id="f8d0f-102">Operação SetToBasisState</span><span class="sxs-lookup"><span data-stu-id="f8d0f-102">SetToBasisState operation</span></span>

<span data-ttu-id="f8d0f-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="f8d0f-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="f8d0f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f8d0f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f8d0f-105">Define um qubit para um determinado estado de base computacional medindo o qubit e aplicando uma inversão de bit, se necessário.</span><span class="sxs-lookup"><span data-stu-id="f8d0f-105">Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.</span></span>

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="f8d0f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8d0f-106">Input</span></span>

### <a name="desired--__invalidresult__"></a><span data-ttu-id="f8d0f-107">desejado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="f8d0f-107">desired : __invalid<Result>__</span></span>

<span data-ttu-id="f8d0f-108">O estado base ao qual o qubit deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="f8d0f-108">The basis state that the qubit should be set to.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f8d0f-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f8d0f-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f8d0f-110">O qubit cujo estado deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="f8d0f-110">The qubit whose state is to be set.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f8d0f-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f8d0f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f8d0f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8d0f-112">Remarks</span></span>

<span data-ttu-id="f8d0f-113">Como uma constante desta operação, chamar `M(q)` imediatamente após `SetToBasisState(result, q)` será retornado `result` .</span><span class="sxs-lookup"><span data-stu-id="f8d0f-113">As an invariant of this operation, calling `M(q)` immediately after `SetToBasisState(result, q)` will return `result`.</span></span>