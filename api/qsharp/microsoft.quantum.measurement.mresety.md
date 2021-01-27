---
uid: Microsoft.Quantum.Measurement.MResetY
title: Operação MResetY
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 2e41e76a46b68178a8a22b39131d6ca2a8c50b64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854648"
---
# <a name="mresety-operation"></a><span data-ttu-id="672ce-102">Operação MResetY</span><span class="sxs-lookup"><span data-stu-id="672ce-102">MResetY operation</span></span>

<span data-ttu-id="672ce-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="672ce-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="672ce-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="672ce-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="672ce-105">Mede um único qubit na base Y e o redefine para um estado inicial fixo após a medição.</span><span class="sxs-lookup"><span data-stu-id="672ce-105">Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="672ce-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="672ce-106">Description</span></span>

<span data-ttu-id="672ce-107">Executa uma medida de qubit único no $Y $-base e garante que o qubit seja retornado para $ \ket {0} $ após a medição.</span><span class="sxs-lookup"><span data-stu-id="672ce-107">Performs a single-qubit measurement in the $Y$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="672ce-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="672ce-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="672ce-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="672ce-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="672ce-110">Um único qubit a ser medido.</span><span class="sxs-lookup"><span data-stu-id="672ce-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="672ce-111">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="672ce-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="672ce-112">O resultado da medição `target` na base Pauli $Y $.</span><span class="sxs-lookup"><span data-stu-id="672ce-112">The result of measuring `target` in the Pauli $Y$ basis.</span></span>