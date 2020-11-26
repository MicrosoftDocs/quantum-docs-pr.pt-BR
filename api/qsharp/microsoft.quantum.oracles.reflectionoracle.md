---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Tipo definido pelo usuário ReflectionOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 7bb0626e7cca9ae0b640699ea57f2e114bda2d06
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226648"
---
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="60b62-102">Tipo definido pelo usuário ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="60b62-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="60b62-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="60b62-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="60b62-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="60b62-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="60b62-105">Representa uma reflexão do Oracle.</span><span class="sxs-lookup"><span data-stu-id="60b62-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="60b62-106">Uma reflexão do Oracle, $O $, tem entradas:</span><span class="sxs-lookup"><span data-stu-id="60b62-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="60b62-107">A fase $ \phi $ pela qual girar o subespaço refletido.</span><span class="sxs-lookup"><span data-stu-id="60b62-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="60b62-108">O qubit se registra no qual executar a reflexão determinada.</span><span class="sxs-lookup"><span data-stu-id="60b62-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="60b62-109">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="60b62-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a><span data-ttu-id="60b62-110">ApplyReflection: ([Double](xref:microsoft.quantum.lang-ref.double),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="60b62-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="60b62-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="60b62-111">Remarks</span></span>

<span data-ttu-id="60b62-112">Este Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ executa uma reflexão parcial por uma fase $ \phi $ sobre um único estado puro $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="60b62-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>