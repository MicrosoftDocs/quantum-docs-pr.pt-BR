---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState operação
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 384dad5905cec50b500028e1bc352a742122b299
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693574"
---
# <a name="_prepareentangledstate-operation"></a><span data-ttu-id="32895-102">_prepareEntangledState operação</span><span class="sxs-lookup"><span data-stu-id="32895-102">_prepareEntangledState operation</span></span>

<span data-ttu-id="32895-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="32895-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="32895-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="32895-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="32895-105">Dadas dois registros, o prepara o estado de confusas máximo entre cada par de qubits nos respectivos registros.</span><span class="sxs-lookup"><span data-stu-id="32895-105">Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers.</span></span>
<span data-ttu-id="32895-106">Todos os qubits devem iniciar no estado | 0 ⟩.</span><span class="sxs-lookup"><span data-stu-id="32895-106">All qubits must start in the |0⟩ state.</span></span>

<span data-ttu-id="32895-107">O resultado é que os pares correspondentes de qubits de cada registro estão no $ \bra{\ beta_ {00} } \ket{\ beta_ {00} } $.</span><span class="sxs-lookup"><span data-stu-id="32895-107">The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.</span></span>

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="32895-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="32895-108">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="32895-109">esquerda: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="32895-109">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="32895-110">Uma matriz qubit no estado $ \ket{0\cdots 0} $</span><span class="sxs-lookup"><span data-stu-id="32895-110">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="32895-111">direita: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="32895-111">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="32895-112">Uma matriz qubit no estado $ \ket{0\cdots 0} $</span><span class="sxs-lookup"><span data-stu-id="32895-112">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="32895-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="32895-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
