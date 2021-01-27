---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterA
title: Função RestrictedToSubregisterA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: c260a0e422d7ffb8137f6ac41e1cb398b2f4a2a7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852190"
---
# <a name="restrictedtosubregistera-function"></a><span data-ttu-id="617c3-102">Função RestrictedToSubregisterA</span><span class="sxs-lookup"><span data-stu-id="617c3-102">RestrictedToSubregisterA function</span></span>

<span data-ttu-id="617c3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="617c3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="617c3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="617c3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="617c3-105">Restringe uma operação a uma matriz de índices de um registro, ou seja, um subregistro.</span><span class="sxs-lookup"><span data-stu-id="617c3-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="617c3-106">O modificador `A` indica que a operação é de adjointable.</span><span class="sxs-lookup"><span data-stu-id="617c3-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function RestrictedToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[]) : (Qubit[] => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="617c3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="617c3-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="617c3-108">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="617c3-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="617c3-109">Operação a ser restrita a um subregistro.</span><span class="sxs-lookup"><span data-stu-id="617c3-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="617c3-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="617c3-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="617c3-111">Matriz de índices, indicando a qual qubits a operação será restrita.</span><span class="sxs-lookup"><span data-stu-id="617c3-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit--is-adj"></a><span data-ttu-id="617c3-112">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="617c3-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>



## <a name="see-also"></a><span data-ttu-id="617c3-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="617c3-113">See Also</span></span>

- [<span data-ttu-id="617c3-114">Microsoft. Quantum. Canon. RestrictedToSubregister</span><span class="sxs-lookup"><span data-stu-id="617c3-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)