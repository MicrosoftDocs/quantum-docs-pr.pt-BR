---
uid: Microsoft.Quantum.Intrinsic.Ry
title: Operação entar
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Ry
qsharp.summary: >-
  Applies a rotation about the $y$-axis by a given angle.

  \begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 5a1f762aacca5c72dc8dbe450ab8e8a4aef12c69
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198598"
---
# <a name="ry-operation"></a><span data-ttu-id="a8d5f-102">Operação entar</span><span class="sxs-lookup"><span data-stu-id="a8d5f-102">Ry operation</span></span>

<span data-ttu-id="a8d5f-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="a8d5f-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="a8d5f-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a8d5f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a8d5f-105">Aplica uma rotação sobre o eixo $ $y por um determinado ângulo.</span><span class="sxs-lookup"><span data-stu-id="a8d5f-105">Applies a rotation about the $y$-axis by a given angle.</span></span>

<span data-ttu-id="a8d5f-106">\begin{align} R_y (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_y/2} = \begin{bmatrix} \cos \frac{\theta} {2} &-\sin \frac{\theta} {2} \\ \\ \sin \frac{\theta} {2} & \cos \frac{\theta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="a8d5f-106">\begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="a8d5f-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="a8d5f-107">\end{align}</span></span>

```qsharp
operation Ry (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a8d5f-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a8d5f-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="a8d5f-109">teta: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a8d5f-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a8d5f-110">Ângulo sobre o qual o qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="a8d5f-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="a8d5f-111">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a8d5f-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a8d5f-112">Qubit ao qual a portão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="a8d5f-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a8d5f-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a8d5f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a8d5f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8d5f-114">Remarks</span></span>

<span data-ttu-id="a8d5f-115">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="a8d5f-115">Equivalent to:</span></span>

```qsharp
R(PauliY, theta, qubit);
```