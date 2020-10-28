---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Operação CCNOT
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: bf20ff1e9d25d72e7e8e0207ab947a57dc394cf4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693346"
---
# <a name="ccnot-operation"></a><span data-ttu-id="dc9be-102">Operação CCNOT</span><span class="sxs-lookup"><span data-stu-id="dc9be-102">CCNOT operation</span></span>

<span data-ttu-id="dc9be-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="dc9be-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="dc9be-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dc9be-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dc9be-105">Aplica o portão duplo (não-CCNOT) controlado a três qubits.</span><span class="sxs-lookup"><span data-stu-id="dc9be-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="dc9be-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc9be-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="dc9be-107">Control1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dc9be-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dc9be-108">Primeiro controle qubit para o portão CCNOT.</span><span class="sxs-lookup"><span data-stu-id="dc9be-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="dc9be-109">Control2: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dc9be-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dc9be-110">Segundo controle qubit para o portão CCNOT.</span><span class="sxs-lookup"><span data-stu-id="dc9be-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="dc9be-111">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dc9be-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dc9be-112">Qubit de destino para o portão CCNOT.</span><span class="sxs-lookup"><span data-stu-id="dc9be-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dc9be-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dc9be-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="dc9be-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc9be-114">Remarks</span></span>

<span data-ttu-id="dc9be-115">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="dc9be-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```