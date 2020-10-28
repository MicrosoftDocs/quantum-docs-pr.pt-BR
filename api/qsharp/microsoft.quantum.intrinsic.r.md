---
uid: Microsoft.Quantum.Intrinsic.R
title: Operação de R
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R
qsharp.summary: >-
  Applies a rotation about the given Pauli axis.

  \begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.
ms.openlocfilehash: 7d1d51031f4587b1c501feab459e614fc1530457
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694753"
---
# <a name="r-operation"></a><span data-ttu-id="511fc-102">Operação de R</span><span class="sxs-lookup"><span data-stu-id="511fc-102">R operation</span></span>

<span data-ttu-id="511fc-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="511fc-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="511fc-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="511fc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="511fc-105">Aplica uma rotação sobre o eixo de Pauli fornecido.</span><span class="sxs-lookup"><span data-stu-id="511fc-105">Applies a rotation about the given Pauli axis.</span></span>

<span data-ttu-id="511fc-106">\begin{align} R_ {\mu} (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_ {\mu}/2}, \end{align} em que $ \mu na \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="511fc-106">\begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

```qsharp
operation R (pauli : Pauli, theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="511fc-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="511fc-107">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="511fc-108">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="511fc-108">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="511fc-109">Operador Pauli ($ \mu $) a ser exponenciação para formar a rotação.</span><span class="sxs-lookup"><span data-stu-id="511fc-109">Pauli operator ($\mu$) to be exponentiated to form the rotation.</span></span>


### <a name="theta--double"></a><span data-ttu-id="511fc-110">teta: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="511fc-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="511fc-111">Ângulo sobre o qual o qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="511fc-111">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="511fc-112">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="511fc-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="511fc-113">Qubit ao qual a portão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="511fc-113">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="511fc-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="511fc-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="511fc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="511fc-115">Remarks</span></span>

<span data-ttu-id="511fc-116">Quando chamado com `pauli = PauliI` , essa operação aplica uma *fase global* .</span><span class="sxs-lookup"><span data-stu-id="511fc-116">When called with `pauli = PauliI`, this operation applies a *global phase* .</span></span> <span data-ttu-id="511fc-117">Essa fase pode ser significativa quando usada com o `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="511fc-117">This phase can be significant when used with the `Controlled` functor.</span></span>