---
uid: Microsoft.Quantum.Intrinsic.Rz
title: Operação RZ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: d637abf3562eb60705da517467939dc588229c39
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198615"
---
# <a name="rz-operation"></a><span data-ttu-id="dfeb4-102">Operação RZ</span><span class="sxs-lookup"><span data-stu-id="dfeb4-102">Rz operation</span></span>

<span data-ttu-id="dfeb4-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="dfeb4-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="dfeb4-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="dfeb4-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="dfeb4-105">Aplica uma rotação sobre o eixo $ $z por um determinado ângulo.</span><span class="sxs-lookup"><span data-stu-id="dfeb4-105">Applies a rotation about the $z$-axis by a given angle.</span></span>

<span data-ttu-id="dfeb4-106">\begin{align} R_z (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_z/2} = \begin{bmatrix} e ^ {-i \theta/2} & 0 \\ \\ 0 & e ^ {i \theta/2} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="dfeb4-106">\begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}.</span></span>
<span data-ttu-id="dfeb4-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="dfeb4-107">\end{align}</span></span>

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="dfeb4-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="dfeb4-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="dfeb4-109">teta: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="dfeb4-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="dfeb4-110">Ângulo sobre o qual o qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="dfeb4-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="dfeb4-111">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dfeb4-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dfeb4-112">Qubit ao qual a portão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="dfeb4-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dfeb4-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dfeb4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="dfeb4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfeb4-114">Remarks</span></span>

<span data-ttu-id="dfeb4-115">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="dfeb4-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
```