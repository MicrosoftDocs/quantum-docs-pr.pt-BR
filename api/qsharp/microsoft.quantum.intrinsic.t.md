---
uid: Microsoft.Quantum.Intrinsic.T
title: Operação T
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: 868031386c95f65ae956b5e444c6d87d7ea0a697
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694740"
---
# <a name="t-operation"></a><span data-ttu-id="63c41-102">Operação T</span><span class="sxs-lookup"><span data-stu-id="63c41-102">T operation</span></span>

<span data-ttu-id="63c41-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="63c41-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="63c41-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="63c41-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="63c41-105">Aplica a entrada T a um único qubit.</span><span class="sxs-lookup"><span data-stu-id="63c41-105">Applies the T gate to a single qubit.</span></span>

```qsharp
operation T (qubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="63c41-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="63c41-106">Description</span></span>

<span data-ttu-id="63c41-107">Esta operação pode ser simulada pela matriz unitário \begin{align} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & e ^ {i \pi/4} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="63c41-107">This operation can be simulated by the unitary matrix \begin{align} T \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \pi / 4} \end{bmatrix}.</span></span>
<span data-ttu-id="63c41-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="63c41-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="63c41-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="63c41-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="63c41-110">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="63c41-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="63c41-111">Qubit ao qual a portão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="63c41-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="63c41-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="63c41-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
