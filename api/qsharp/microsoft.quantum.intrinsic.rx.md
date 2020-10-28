---
uid: Microsoft.Quantum.Intrinsic.Rx
title: Operação RX
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rx
qsharp.summary: >-
  Applies a rotation about the $x$-axis by a given angle.

  \begin{align} R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -i\sin \frac{\theta}{2}  \\\\ -i\sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 6d11c8fa3c3fb2c07a88fdf2cba0ff2a7f51bf6b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696809"
---
# <a name="rx-operation"></a><span data-ttu-id="e1bc3-102">Operação RX</span><span class="sxs-lookup"><span data-stu-id="e1bc3-102">Rx operation</span></span>

<span data-ttu-id="e1bc3-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="e1bc3-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="e1bc3-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e1bc3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e1bc3-105">Aplica uma rotação sobre o eixo $ $x por um determinado ângulo.</span><span class="sxs-lookup"><span data-stu-id="e1bc3-105">Applies a rotation about the $x$-axis by a given angle.</span></span>

<span data-ttu-id="e1bc3-106">\begin{align} R_x (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_x/2} = \begin{bmatrix} \cos \frac{\theta} {2} &-i\sin \frac{\theta} {2} \\ \\ -i\sin \frac{\theta} {2} & \cos \frac{\theta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="e1bc3-106">\begin{align} R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -i\sin \frac{\theta}{2}  \\\\ -i\sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="e1bc3-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="e1bc3-107">\end{align}</span></span>

```qsharp
operation Rx (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="e1bc3-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1bc3-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="e1bc3-109">teta: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e1bc3-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e1bc3-110">Ângulo sobre o qual o qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="e1bc3-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="e1bc3-111">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e1bc3-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e1bc3-112">Qubit ao qual a portão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="e1bc3-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e1bc3-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e1bc3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e1bc3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1bc3-114">Remarks</span></span>

<span data-ttu-id="e1bc3-115">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="e1bc3-115">Equivalent to:</span></span>

```qsharp
R(PauliX, theta, qubit);
```