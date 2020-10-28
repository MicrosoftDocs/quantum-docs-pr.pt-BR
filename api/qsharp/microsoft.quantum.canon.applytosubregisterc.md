---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterC
title: Operação ApplyToSubregisterC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterC
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: ba5be1e7e822197eb76aac029be8617a70d51ddb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694127"
---
# <a name="applytosubregisterc-operation"></a><span data-ttu-id="d72c2-102">Operação ApplyToSubregisterC</span><span class="sxs-lookup"><span data-stu-id="d72c2-102">ApplyToSubregisterC operation</span></span>

<span data-ttu-id="d72c2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d72c2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d72c2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d72c2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d72c2-105">Aplica uma operação a um subregistro de um registro, com qubits especificado por uma matriz de seus índices.</span><span class="sxs-lookup"><span data-stu-id="d72c2-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="d72c2-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="d72c2-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d72c2-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d72c2-107">Input</span></span>

### <a name="op--qubit--unit-ctl"></a><span data-ttu-id="d72c2-108">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d72c2-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="d72c2-109">Operação a ser aplicada ao subregistro.</span><span class="sxs-lookup"><span data-stu-id="d72c2-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="d72c2-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d72c2-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d72c2-111">Matriz de índices, indicando a qual qubits a operação será aplicada.</span><span class="sxs-lookup"><span data-stu-id="d72c2-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d72c2-112">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d72c2-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d72c2-113">Registrar em que a operação atua.</span><span class="sxs-lookup"><span data-stu-id="d72c2-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d72c2-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d72c2-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="d72c2-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d72c2-115">See Also</span></span>

- [<span data-ttu-id="d72c2-116">Microsoft. Quantum. Canon. ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="d72c2-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)