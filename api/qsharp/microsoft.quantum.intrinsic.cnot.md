---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: Operação CNOT
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 90e84f7d0ea7373498632474dfafa23335f0c78e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198967"
---
# <a name="cnot-operation"></a><span data-ttu-id="7f7f6-102">Operação CNOT</span><span class="sxs-lookup"><span data-stu-id="7f7f6-102">CNOT operation</span></span>

<span data-ttu-id="7f7f6-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="7f7f6-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="7f7f6-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7f7f6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7f7f6-105">Aplica o portão-NOT (CNOT) controlado a um par de qubits.</span><span class="sxs-lookup"><span data-stu-id="7f7f6-105">Applies the controlled-NOT (CNOT) gate to a pair of qubits.</span></span>

<span data-ttu-id="7f7f6-106">\begin{align} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="7f7f6-106">\begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="7f7f6-107">onde as linhas e colunas são ordenadas como no guia de conceitos do Quantum.</span><span class="sxs-lookup"><span data-stu-id="7f7f6-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7f7f6-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="7f7f6-108">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="7f7f6-109">controle: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7f7f6-109">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7f7f6-110">Controle qubit para o portão CNOT.</span><span class="sxs-lookup"><span data-stu-id="7f7f6-110">Control qubit for the CNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="7f7f6-111">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7f7f6-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7f7f6-112">Qubit de destino para o portão CNOT.</span><span class="sxs-lookup"><span data-stu-id="7f7f6-112">Target qubit for the CNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7f7f6-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7f7f6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7f7f6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f7f6-114">Remarks</span></span>

<span data-ttu-id="7f7f6-115">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="7f7f6-115">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```