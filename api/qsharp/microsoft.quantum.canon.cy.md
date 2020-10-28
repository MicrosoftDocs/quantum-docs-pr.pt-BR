---
uid: Microsoft.Quantum.Canon.CY
title: Operação CY
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 291891457ff39cf7092d17aa1d900dd0d35d9cf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694035"
---
# <a name="cy-operation"></a><span data-ttu-id="b496d-102">Operação CY</span><span class="sxs-lookup"><span data-stu-id="b496d-102">CY operation</span></span>

<span data-ttu-id="b496d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b496d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b496d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b496d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b496d-105">Aplica a porta x (CY) controlada a um par de qubits.</span><span class="sxs-lookup"><span data-stu-id="b496d-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="b496d-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & i & 0 \end{Align}, $ $, em que as linhas e colunas são organizadas como no guia de conceitos do Quantum.</span><span class="sxs-lookup"><span data-stu-id="b496d-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="b496d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b496d-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="b496d-108">controle: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b496d-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b496d-109">Controle qubit para o portão CY.</span><span class="sxs-lookup"><span data-stu-id="b496d-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="b496d-110">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b496d-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b496d-111">Qubit de destino para o portão CY.</span><span class="sxs-lookup"><span data-stu-id="b496d-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b496d-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b496d-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b496d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b496d-113">Remarks</span></span>

<span data-ttu-id="b496d-114">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="b496d-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```