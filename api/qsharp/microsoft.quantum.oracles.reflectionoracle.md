---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Tipo definido pelo usuário ReflectionOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 8e35e7e508ea7e0c30ea2a70633f71a6c87d4be1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696910"
---
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="9ed67-102">Tipo definido pelo usuário ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="9ed67-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="9ed67-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="9ed67-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="9ed67-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9ed67-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9ed67-105">Representa uma reflexão do Oracle.</span><span class="sxs-lookup"><span data-stu-id="9ed67-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="9ed67-106">Uma reflexão do Oracle, $O $, tem entradas:</span><span class="sxs-lookup"><span data-stu-id="9ed67-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="9ed67-107">A fase $ \phi $ pela qual girar o subespaço refletido.</span><span class="sxs-lookup"><span data-stu-id="9ed67-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="9ed67-108">O qubit se registra no qual executar a reflexão determinada.</span><span class="sxs-lookup"><span data-stu-id="9ed67-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="9ed67-109">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="9ed67-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit-adj--ctl"></a><span data-ttu-id="9ed67-110">ApplyReflection: ([Double](xref:microsoft.quantum.lang-ref.double),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit) adj + CTL</span><span class="sxs-lookup"><span data-stu-id="9ed67-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="9ed67-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ed67-111">Remarks</span></span>

<span data-ttu-id="9ed67-112">Este Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ executa uma reflexão parcial por uma fase $ \phi $ sobre um único estado puro $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="9ed67-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>