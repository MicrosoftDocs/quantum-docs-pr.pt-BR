---
uid: Microsoft.Quantum.Measurement.MResetX
title: Operação MResetX
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 44459e681daf1d28ce7d45f91ad59059babe5716
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853751"
---
# <a name="mresetx-operation"></a><span data-ttu-id="084ee-102">Operação MResetX</span><span class="sxs-lookup"><span data-stu-id="084ee-102">MResetX operation</span></span>

<span data-ttu-id="084ee-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="084ee-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="084ee-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="084ee-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="084ee-105">Mede um único qubit na base X e o redefine para um estado inicial fixo após a medição.</span><span class="sxs-lookup"><span data-stu-id="084ee-105">Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="084ee-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="084ee-106">Description</span></span>

<span data-ttu-id="084ee-107">Executa uma medida de qubit único no $X $-base e garante que o qubit seja retornado para $ \ket {0} $ após a medição.</span><span class="sxs-lookup"><span data-stu-id="084ee-107">Performs a single-qubit measurement in the $X$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="084ee-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="084ee-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="084ee-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="084ee-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="084ee-110">Um único qubit a ser medido.</span><span class="sxs-lookup"><span data-stu-id="084ee-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="084ee-111">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="084ee-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="084ee-112">O resultado da medição `target` na base Pauli $X $.</span><span class="sxs-lookup"><span data-stu-id="084ee-112">The result of measuring `target` in the Pauli $X$ basis.</span></span>