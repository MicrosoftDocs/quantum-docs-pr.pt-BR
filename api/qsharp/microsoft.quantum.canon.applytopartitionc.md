---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: Operação ApplyToPartitionC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 43cf43fa2bf9c00a4096b39555b8f6080dd506d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850520"
---
# <a name="applytopartitionc-operation"></a><span data-ttu-id="2bf67-102">Operação ApplyToPartitionC</span><span class="sxs-lookup"><span data-stu-id="2bf67-102">ApplyToPartitionC operation</span></span>

<span data-ttu-id="2bf67-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2bf67-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2bf67-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2bf67-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2bf67-105">Aplica um par de operações a uma determinada partição de um registro em duas partes.</span><span class="sxs-lookup"><span data-stu-id="2bf67-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="2bf67-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="2bf67-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="2bf67-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2bf67-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-ctl"></a><span data-ttu-id="2bf67-108">op: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL</span><span class="sxs-lookup"><span data-stu-id="2bf67-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="2bf67-109">O par de operações a serem aplicadas à partição especificada.</span><span class="sxs-lookup"><span data-stu-id="2bf67-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="2bf67-110">numberOfQubitsToFirstArgument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2bf67-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2bf67-111">Número de qubits do destino a ser colocado na primeira parte da partição.</span><span class="sxs-lookup"><span data-stu-id="2bf67-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="2bf67-112">O qubits restante constitui a segunda parte da partição.</span><span class="sxs-lookup"><span data-stu-id="2bf67-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="2bf67-113">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="2bf67-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="2bf67-114">Um registro de qubits que estão sendo particionados e operados pela determinada operação.</span><span class="sxs-lookup"><span data-stu-id="2bf67-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2bf67-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2bf67-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="2bf67-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2bf67-116">See Also</span></span>

- [<span data-ttu-id="2bf67-117">Microsoft. Quantum. Canon. ApplyToPartition</span><span class="sxs-lookup"><span data-stu-id="2bf67-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)