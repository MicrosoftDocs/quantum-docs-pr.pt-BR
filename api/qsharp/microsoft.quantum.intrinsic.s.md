---
uid: Microsoft.Quantum.Intrinsic.S
title: Operação S
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: S
qsharp.summary: Applies the S gate to a single qubit.
ms.openlocfilehash: be9078dfdcc4eecf317b0542b1c42a8d60466a5f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817526"
---
# <a name="s-operation"></a><span data-ttu-id="4241f-102">Operação S</span><span class="sxs-lookup"><span data-stu-id="4241f-102">S operation</span></span>

<span data-ttu-id="4241f-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="4241f-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="4241f-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4241f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="4241f-105">Aplica o portão S a um único qubit.</span><span class="sxs-lookup"><span data-stu-id="4241f-105">Applies the S gate to a single qubit.</span></span>

```qsharp
operation S (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="4241f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4241f-106">Description</span></span>

<span data-ttu-id="4241f-107">Esta operação pode ser simulada pela matriz unitário \begin{align} S \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & i \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="4241f-107">This operation can be simulated by the unitary matrix \begin{align} S \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="4241f-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="4241f-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="4241f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="4241f-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="4241f-110">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="4241f-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="4241f-111">Qubit ao qual a portão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="4241f-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4241f-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4241f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

