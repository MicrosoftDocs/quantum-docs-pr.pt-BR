---
uid: Microsoft.Quantum.Canon.CX
title: Operação CX
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: c430525b71ad4ef0812d90a8ff20c41a5d5b8708
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694037"
---
# <a name="cx-operation"></a><span data-ttu-id="0ff63-102">Operação CX</span><span class="sxs-lookup"><span data-stu-id="0ff63-102">CX operation</span></span>

<span data-ttu-id="0ff63-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0ff63-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0ff63-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0ff63-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0ff63-105">Aplica o portão X (CX) controlado a um par de qubits.</span><span class="sxs-lookup"><span data-stu-id="0ff63-105">Applies the controlled-X (CX) gate to a pair of qubits.</span></span>

<span data-ttu-id="0ff63-106">$ $ \begin{align} \left (\begin{Matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{Matrix}\right) \end{Align}, $ $ em que as linhas e colunas são organizadas como no guia de conceitos do Quantum.</span><span class="sxs-lookup"><span data-stu-id="0ff63-106">$$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="0ff63-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0ff63-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="0ff63-108">controle: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0ff63-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0ff63-109">Controle qubit para o portão CX.</span><span class="sxs-lookup"><span data-stu-id="0ff63-109">Control qubit for the CX gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="0ff63-110">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0ff63-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0ff63-111">Qubit de destino para o portão CX.</span><span class="sxs-lookup"><span data-stu-id="0ff63-111">Target qubit for the CX gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0ff63-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0ff63-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0ff63-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ff63-113">Remarks</span></span>

<span data-ttu-id="0ff63-114">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="0ff63-114">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```

<span data-ttu-id="0ff63-115">e para:</span><span class="sxs-lookup"><span data-stu-id="0ff63-115">and to:</span></span>

```qsharp
CNOT(control, target);
```