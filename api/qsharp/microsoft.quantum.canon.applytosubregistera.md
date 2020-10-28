---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterA
title: Operação ApplyToSubregisterA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: e0c546b768320ce43e7b44242d15838194e1089d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694130"
---
# <a name="applytosubregistera-operation"></a><span data-ttu-id="3435d-102">Operação ApplyToSubregisterA</span><span class="sxs-lookup"><span data-stu-id="3435d-102">ApplyToSubregisterA operation</span></span>

<span data-ttu-id="3435d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3435d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3435d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3435d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3435d-105">Aplica uma operação a um subregistro de um registro, com qubits especificado por uma matriz de seus índices.</span><span class="sxs-lookup"><span data-stu-id="3435d-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="3435d-106">O modificador `A` indica que a operação é de adjointable.</span><span class="sxs-lookup"><span data-stu-id="3435d-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="3435d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="3435d-107">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="3435d-108">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3435d-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="3435d-109">Operação a ser aplicada ao subregistro.</span><span class="sxs-lookup"><span data-stu-id="3435d-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="3435d-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3435d-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="3435d-111">Matriz de índices, indicando a qual qubits a operação será aplicada.</span><span class="sxs-lookup"><span data-stu-id="3435d-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="3435d-112">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3435d-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3435d-113">Registrar em que a operação atua.</span><span class="sxs-lookup"><span data-stu-id="3435d-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3435d-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3435d-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="3435d-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3435d-115">See Also</span></span>

- [<span data-ttu-id="3435d-116">Microsoft. Quantum. Canon. ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="3435d-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)