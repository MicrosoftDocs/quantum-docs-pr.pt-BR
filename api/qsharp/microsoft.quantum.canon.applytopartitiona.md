---
uid: Microsoft.Quantum.Canon.ApplyToPartitionA
title: Operação ApplyToPartitionA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionA
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 6ff3bf8b5a4344ee5a7a054c6285a5492260068d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694145"
---
# <a name="applytopartitiona-operation"></a><span data-ttu-id="64948-102">Operação ApplyToPartitionA</span><span class="sxs-lookup"><span data-stu-id="64948-102">ApplyToPartitionA operation</span></span>

<span data-ttu-id="64948-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="64948-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="64948-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="64948-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="64948-105">Aplica um par de operações a uma determinada partição de um registro em duas partes.</span><span class="sxs-lookup"><span data-stu-id="64948-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="64948-106">O modificador `A` indica que a operação é de adjointable.</span><span class="sxs-lookup"><span data-stu-id="64948-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToPartitionA (op : ((Qubit[], Qubit[]) => Unit is Adj), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="64948-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="64948-107">Input</span></span>

### <a name="op--qubitqubit--unit-adj"></a><span data-ttu-id="64948-108">op: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64948-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="64948-109">O par de operações a serem aplicadas à partição especificada.</span><span class="sxs-lookup"><span data-stu-id="64948-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="64948-110">numberOfQubitsToFirstArgument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="64948-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="64948-111">Número de qubits do destino a ser colocado na primeira parte da partição.</span><span class="sxs-lookup"><span data-stu-id="64948-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="64948-112">O qubits restante constitui a segunda parte da partição.</span><span class="sxs-lookup"><span data-stu-id="64948-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="64948-113">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="64948-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="64948-114">Um registro de qubits que estão sendo particionados e operados pela determinada operação.</span><span class="sxs-lookup"><span data-stu-id="64948-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="64948-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64948-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="64948-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="64948-116">See Also</span></span>

- [<span data-ttu-id="64948-117">Microsoft. Quantum. Canon. ApplyToPartition</span><span class="sxs-lookup"><span data-stu-id="64948-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)