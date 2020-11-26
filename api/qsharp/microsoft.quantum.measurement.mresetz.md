---
uid: Microsoft.Quantum.Measurement.MResetZ
title: Operação MResetZ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 494f11c8129175ddd84c6539f5e9df1a758e8a82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194127"
---
# <a name="mresetz-operation"></a><span data-ttu-id="335bc-102">Operação MResetZ</span><span class="sxs-lookup"><span data-stu-id="335bc-102">MResetZ operation</span></span>

<span data-ttu-id="335bc-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="335bc-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="335bc-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="335bc-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="335bc-105">Mede um único qubit na base Z e o redefine para um estado inicial fixo após a medição.</span><span class="sxs-lookup"><span data-stu-id="335bc-105">Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="335bc-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="335bc-106">Description</span></span>

<span data-ttu-id="335bc-107">Executa uma medida de qubit único no $Z $-base e garante que o qubit seja retornado para $ \ket {0} $ após a medição.</span><span class="sxs-lookup"><span data-stu-id="335bc-107">Performs a single-qubit measurement in the $Z$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="335bc-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="335bc-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="335bc-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="335bc-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="335bc-110">Um único qubit a ser medido.</span><span class="sxs-lookup"><span data-stu-id="335bc-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="335bc-111">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="335bc-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="335bc-112">O resultado da medição `target` na base Pauli $Z $.</span><span class="sxs-lookup"><span data-stu-id="335bc-112">The result of measuring `target` in the Pauli $Z$ basis.</span></span>