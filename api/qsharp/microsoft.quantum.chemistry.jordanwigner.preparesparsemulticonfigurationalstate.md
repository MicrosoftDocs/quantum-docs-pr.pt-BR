---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareSparseMultiConfigurationalState
title: Operação PrepareSparseMultiConfigurationalState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareSparseMultiConfigurationalState
qsharp.summary: Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.
ms.openlocfilehash: 1182f79a33784cdb49cb13db5cc97a0a45e59f9f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693676"
---
# <a name="preparesparsemulticonfigurationalstate-operation"></a><span data-ttu-id="92310-102">Operação PrepareSparseMultiConfigurationalState</span><span class="sxs-lookup"><span data-stu-id="92310-102">PrepareSparseMultiConfigurationalState operation</span></span>

<span data-ttu-id="92310-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="92310-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="92310-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="92310-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="92310-105">Preparação de estado de várias configurações esparsas do estado de avaliação adicionando excitations ao estado de avaliação inicial.</span><span class="sxs-lookup"><span data-stu-id="92310-105">Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.</span></span>

```qsharp
operation PrepareSparseMultiConfigurationalState (initialStatePreparation : (Qubit[] => Unit), excitations : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="92310-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="92310-106">Input</span></span>

### <a name="initialstatepreparation--qubit--unit"></a><span data-ttu-id="92310-107">initialStatePreparation: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="92310-107">initialStatePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="92310-108">Unitário para preparar o estado de avaliação inicial.</span><span class="sxs-lookup"><span data-stu-id="92310-108">Unitary to prepare initial trial state.</span></span>


### <a name="excitations--jordanwignerinputstate"></a><span data-ttu-id="92310-109">excitations: [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="92310-109">excitations : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>

<span data-ttu-id="92310-110">Excitations do estado de avaliação inicial representado pela amplitude do Excitation e os índices qubit nos quais o Excitation atua.</span><span class="sxs-lookup"><span data-stu-id="92310-110">Excitations of initial trial state represented by the amplitude of the excitation and the qubit indices the excitation acts on.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="92310-111">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="92310-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="92310-112">Qubits Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="92310-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="92310-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="92310-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
