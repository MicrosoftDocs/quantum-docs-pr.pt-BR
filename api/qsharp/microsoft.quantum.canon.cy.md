---
uid: Microsoft.Quantum.Canon.CY
title: Operação CY
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 862f058e630ee6d9159e0fe514ca2dd1179ea9a2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840729"
---
# <a name="cy-operation"></a><span data-ttu-id="be565-102">Operação CY</span><span class="sxs-lookup"><span data-stu-id="be565-102">CY operation</span></span>

<span data-ttu-id="be565-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="be565-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="be565-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="be565-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="be565-105">Aplica a porta x (CY) controlada a um par de qubits.</span><span class="sxs-lookup"><span data-stu-id="be565-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="be565-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & i & 0 \end{Align}, $ $, em que as linhas e colunas são organizadas como no guia de conceitos do Quantum.</span><span class="sxs-lookup"><span data-stu-id="be565-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="be565-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="be565-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="be565-108">controle: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="be565-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="be565-109">Controle qubit para o portão CY.</span><span class="sxs-lookup"><span data-stu-id="be565-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="be565-110">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="be565-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="be565-111">Qubit de destino para o portão CY.</span><span class="sxs-lookup"><span data-stu-id="be565-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="be565-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="be565-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="be565-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="be565-113">Remarks</span></span>

<span data-ttu-id="be565-114">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="be565-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```