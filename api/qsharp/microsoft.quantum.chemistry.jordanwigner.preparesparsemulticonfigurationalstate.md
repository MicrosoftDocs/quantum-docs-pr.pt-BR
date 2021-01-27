---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareSparseMultiConfigurationalState
title: Operação PrepareSparseMultiConfigurationalState
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareSparseMultiConfigurationalState
qsharp.summary: Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.
ms.openlocfilehash: 49b93d0f2447e9eee503bb6ee26aef46c4f5e3f2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98836059"
---
# <a name="preparesparsemulticonfigurationalstate-operation"></a><span data-ttu-id="1dc27-102">Operação PrepareSparseMultiConfigurationalState</span><span class="sxs-lookup"><span data-stu-id="1dc27-102">PrepareSparseMultiConfigurationalState operation</span></span>

<span data-ttu-id="1dc27-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="1dc27-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="1dc27-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="1dc27-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="1dc27-105">Preparação de estado de várias configurações esparsas do estado de avaliação adicionando excitations ao estado de avaliação inicial.</span><span class="sxs-lookup"><span data-stu-id="1dc27-105">Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.</span></span>

```qsharp
operation PrepareSparseMultiConfigurationalState (initialStatePreparation : (Qubit[] => Unit), excitations : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="1dc27-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1dc27-106">Input</span></span>

### <a name="initialstatepreparation--qubit--unit"></a><span data-ttu-id="1dc27-107">initialStatePreparation: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="1dc27-107">initialStatePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="1dc27-108">Unitário para preparar o estado de avaliação inicial.</span><span class="sxs-lookup"><span data-stu-id="1dc27-108">Unitary to prepare initial trial state.</span></span>


### <a name="excitations--jordanwignerinputstate"></a><span data-ttu-id="1dc27-109">excitations: [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="1dc27-109">excitations : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>

<span data-ttu-id="1dc27-110">Excitations do estado de avaliação inicial representado pela amplitude do Excitation e os índices qubit nos quais o Excitation atua.</span><span class="sxs-lookup"><span data-stu-id="1dc27-110">Excitations of initial trial state represented by the amplitude of the excitation and the qubit indices the excitation acts on.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="1dc27-111">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1dc27-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1dc27-112">Qubits Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="1dc27-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1dc27-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1dc27-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

