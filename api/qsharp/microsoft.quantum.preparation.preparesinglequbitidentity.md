---
uid: Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity
title: Operação PrepareSingleQubitIdentity
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareSingleQubitIdentity
qsharp.summary: >-
  Prepares a qubit in the maximally mixed state.

  It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.
ms.openlocfilehash: 1c8c161ec2eae73a81c46e7941af49145cde0493
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193617"
---
# <a name="preparesinglequbitidentity-operation"></a><span data-ttu-id="b3c7d-102">Operação PrepareSingleQubitIdentity</span><span class="sxs-lookup"><span data-stu-id="b3c7d-102">PrepareSingleQubitIdentity operation</span></span>

<span data-ttu-id="b3c7d-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="b3c7d-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="b3c7d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b3c7d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b3c7d-105">Prepara um qubit no estado máximo misto.</span><span class="sxs-lookup"><span data-stu-id="b3c7d-105">Prepares a qubit in the maximally mixed state.</span></span>

<span data-ttu-id="b3c7d-106">Ele prepara o determinado qubit no estado $ \boldone/$2 aplicando o \rho de despolarização do canal $ $ \begin{align} \Omega (\mathrel{): =} \frac {1} {4} \ sum_ {\mu na \{ 0, 1, 2, 3 \} } \sigma \_ {\mu} \rho \sigma \_ {\mu} ^ {\dagger}, \end{Align} $ $, em que $ \sigma \_ i $ é o operador $i $ th Pauli e em que $ \rho $ é um operador de densidade que representa um estado misto.</span><span class="sxs-lookup"><span data-stu-id="b3c7d-106">It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.</span></span>

```qsharp
operation PrepareSingleQubitIdentity (qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="b3c7d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b3c7d-107">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="b3c7d-108">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b3c7d-108">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b3c7d-109">Um qubit cujo estado deve ser depolarizado da maneira descrita acima.</span><span class="sxs-lookup"><span data-stu-id="b3c7d-109">A qubit whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b3c7d-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b3c7d-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b3c7d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3c7d-111">Remarks</span></span>

<span data-ttu-id="b3c7d-112">O estado misto $ \boldone/$2 que descreve o resultado da aplicação dessa operação a um estado descreve implicitamente um valor de expectativa sobre as escolhas aleatórias feitas nesta operação.</span><span class="sxs-lookup"><span data-stu-id="b3c7d-112">The mixed state $\boldone / 2$ describing the result of applying this operation to a state implicitly describes an expectation value over random choices made in this operation.</span></span>
<span data-ttu-id="b3c7d-113">Portanto, para qualquer aplicativo único, essa operação mapeia Estados puros para Estados puros, mas atua conforme descrito em expectativa.</span><span class="sxs-lookup"><span data-stu-id="b3c7d-113">Thus, for any single application, this operation maps pure states to pure states, but it acts as described in expectation.</span></span>
<span data-ttu-id="b3c7d-114">Em particular, essa operação pode ser usada no processo tomography para medir os componentes *não-unitários* de um canal.</span><span class="sxs-lookup"><span data-stu-id="b3c7d-114">In particular, this operation can be used in process tomography to measure the *non-unital* components of a channel.</span></span>