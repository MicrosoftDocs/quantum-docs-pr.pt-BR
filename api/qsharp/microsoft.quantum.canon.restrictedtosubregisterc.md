---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterC
title: Função RestrictedToSubregisterC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterC
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2ca32cf8c85f33f498a30f71833b3dd69db6da6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693914"
---
# <a name="restrictedtosubregisterc-function"></a><span data-ttu-id="4fc2d-102">Função RestrictedToSubregisterC</span><span class="sxs-lookup"><span data-stu-id="4fc2d-102">RestrictedToSubregisterC function</span></span>

<span data-ttu-id="4fc2d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4fc2d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4fc2d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4fc2d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4fc2d-105">Restringe uma operação a uma matriz de índices de um registro, ou seja, um subregistro.</span><span class="sxs-lookup"><span data-stu-id="4fc2d-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="4fc2d-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="4fc2d-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
function RestrictedToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[]) : (Qubit[] => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="4fc2d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="4fc2d-107">Input</span></span>

### <a name="op--qubit--unit-ctl"></a><span data-ttu-id="4fc2d-108">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4fc2d-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="4fc2d-109">Operação a ser restrita a um subregistro.</span><span class="sxs-lookup"><span data-stu-id="4fc2d-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="4fc2d-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="4fc2d-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="4fc2d-111">Matriz de índices, indicando a qual qubits a operação será restrita.</span><span class="sxs-lookup"><span data-stu-id="4fc2d-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit-ctl"></a><span data-ttu-id="4fc2d-112">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4fc2d-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="4fc2d-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4fc2d-113">See Also</span></span>

- [<span data-ttu-id="4fc2d-114">Microsoft. Quantum. Canon. RestrictedToSubregister</span><span class="sxs-lookup"><span data-stu-id="4fc2d-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)