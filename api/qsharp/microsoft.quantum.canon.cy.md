---
uid: Microsoft.Quantum.Canon.CY
title: Operação CY
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 4a1a533421dd9205e973d5e8237d67b20bc4886d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216567"
---
# <a name="cy-operation"></a><span data-ttu-id="fc357-102">Operação CY</span><span class="sxs-lookup"><span data-stu-id="fc357-102">CY operation</span></span>

<span data-ttu-id="fc357-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fc357-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fc357-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fc357-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fc357-105">Aplica a porta x (CY) controlada a um par de qubits.</span><span class="sxs-lookup"><span data-stu-id="fc357-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="fc357-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & i & 0 \end{Align}, $ $, em que as linhas e colunas são organizadas como no guia de conceitos do Quantum.</span><span class="sxs-lookup"><span data-stu-id="fc357-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="fc357-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="fc357-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="fc357-108">controle: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fc357-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fc357-109">Controle qubit para o portão CY.</span><span class="sxs-lookup"><span data-stu-id="fc357-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="fc357-110">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fc357-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fc357-111">Qubit de destino para o portão CY.</span><span class="sxs-lookup"><span data-stu-id="fc357-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fc357-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fc357-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fc357-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc357-113">Remarks</span></span>

<span data-ttu-id="fc357-114">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="fc357-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```