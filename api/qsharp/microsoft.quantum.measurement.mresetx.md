---
uid: Microsoft.Quantum.Measurement.MResetX
title: Operação MResetX
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 04fb0f84ddf79a3d2cfc21fdaabd16c129f6d72f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194195"
---
# <a name="mresetx-operation"></a><span data-ttu-id="61c39-102">Operação MResetX</span><span class="sxs-lookup"><span data-stu-id="61c39-102">MResetX operation</span></span>

<span data-ttu-id="61c39-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="61c39-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="61c39-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="61c39-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="61c39-105">Mede um único qubit na base X e o redefine para um estado inicial fixo após a medição.</span><span class="sxs-lookup"><span data-stu-id="61c39-105">Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="61c39-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="61c39-106">Description</span></span>

<span data-ttu-id="61c39-107">Executa uma medida de qubit único no $X $-base e garante que o qubit seja retornado para $ \ket {0} $ após a medição.</span><span class="sxs-lookup"><span data-stu-id="61c39-107">Performs a single-qubit measurement in the $X$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="61c39-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="61c39-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="61c39-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="61c39-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="61c39-110">Um único qubit a ser medido.</span><span class="sxs-lookup"><span data-stu-id="61c39-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="61c39-111">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="61c39-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="61c39-112">O resultado da medição `target` na base Pauli $X $.</span><span class="sxs-lookup"><span data-stu-id="61c39-112">The result of measuring `target` in the Pauli $X$ basis.</span></span>