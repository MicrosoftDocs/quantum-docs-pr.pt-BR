---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareUnitaryCoupledClusterState
title: Operação PrepareUnitaryCoupledClusterState
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareUnitaryCoupledClusterState
qsharp.summary: Unitary coupled-cluster state preparation of trial state
ms.openlocfilehash: 1d5b8963bd50752fef22fea0a3c002e3e2ebc90a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98836044"
---
# <a name="prepareunitarycoupledclusterstate-operation"></a><span data-ttu-id="ec190-102">Operação PrepareUnitaryCoupledClusterState</span><span class="sxs-lookup"><span data-stu-id="ec190-102">PrepareUnitaryCoupledClusterState operation</span></span>

<span data-ttu-id="ec190-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="ec190-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="ec190-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ec190-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="ec190-105">Preparação de estado de cluster acoplado unitário do estado de avaliação</span><span class="sxs-lookup"><span data-stu-id="ec190-105">Unitary coupled-cluster state preparation of trial state</span></span>

```qsharp
operation PrepareUnitaryCoupledClusterState (initialStatePreparation : (Qubit[] => Unit), clusterOperator : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], trotterStepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="ec190-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec190-106">Input</span></span>

### <a name="initialstatepreparation--qubit--unit"></a><span data-ttu-id="ec190-107">initialStatePreparation: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="ec190-107">initialStatePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ec190-108">Unitário para preparar o estado de avaliação inicial.</span><span class="sxs-lookup"><span data-stu-id="ec190-108">Unitary to prepare initial trial state.</span></span>


### <a name="clusteroperator--jordanwignerinputstate"></a><span data-ttu-id="ec190-109">clusterOperator: [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="ec190-109">clusterOperator : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>




### <a name="trotterstepsize--double"></a><span data-ttu-id="ec190-110">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ec190-110">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="qubits--qubit"></a><span data-ttu-id="ec190-111">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ec190-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ec190-112">Qubits Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="ec190-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ec190-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec190-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

