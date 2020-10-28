---
uid: Microsoft.Quantum.Intrinsic.R1
title: Operação de R1
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by a given angle.

  \begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}). \end{align}
ms.openlocfilehash: 87302a4338af144ee6a8cec83ed1803581597482
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694751"
---
# <a name="r1-operation"></a><span data-ttu-id="f6da6-102">Operação de R1</span><span class="sxs-lookup"><span data-stu-id="f6da6-102">R1 operation</span></span>

<span data-ttu-id="f6da6-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="f6da6-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="f6da6-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f6da6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f6da6-105">Aplica uma rotação sobre o estado $ \ket {1} $ por um determinado ângulo.</span><span class="sxs-lookup"><span data-stu-id="f6da6-105">Applies a rotation about the $\ket{1}$ state by a given angle.</span></span>

<span data-ttu-id="f6da6-106">\begin{align} R_1 (\theta) \mathrel{: =} \operatorname{diag} (1, e ^ {i\theta}).</span><span class="sxs-lookup"><span data-stu-id="f6da6-106">\begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}).</span></span>
<span data-ttu-id="f6da6-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="f6da6-107">\end{align}</span></span>

```qsharp
operation R1 (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="f6da6-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="f6da6-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="f6da6-109">teta: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f6da6-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f6da6-110">Ângulo sobre o qual o qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="f6da6-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="f6da6-111">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f6da6-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f6da6-112">Qubit ao qual a portão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="f6da6-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f6da6-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f6da6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f6da6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6da6-114">Remarks</span></span>

<span data-ttu-id="f6da6-115">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="f6da6-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
R(PauliI, -theta, qubit);
```