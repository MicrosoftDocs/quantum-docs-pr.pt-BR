---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterCA
title: Função RestrictedToSubregisterCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterCA
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9b1c8a6d1c843fb0533af16aafc4b3ca2ba2f0e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852181"
---
# <a name="restrictedtosubregisterca-function"></a><span data-ttu-id="66567-102">Função RestrictedToSubregisterCA</span><span class="sxs-lookup"><span data-stu-id="66567-102">RestrictedToSubregisterCA function</span></span>

<span data-ttu-id="66567-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="66567-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="66567-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66567-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66567-105">Restringe uma operação a uma matriz de índices de um registro, ou seja, um subregistro.</span><span class="sxs-lookup"><span data-stu-id="66567-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="66567-106">O modificador `CA` indica que a operação é controlável e de adjointable.</span><span class="sxs-lookup"><span data-stu-id="66567-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function RestrictedToSubregisterCA (op : (Qubit[] => Unit is Adj + Ctl), idxs : Int[]) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="66567-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="66567-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="66567-108">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="66567-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="66567-109">Operação a ser restrita a um subregistro.</span><span class="sxs-lookup"><span data-stu-id="66567-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="66567-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="66567-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="66567-111">Matriz de índices, indicando a qual qubits a operação será restrita.</span><span class="sxs-lookup"><span data-stu-id="66567-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="66567-112">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="66567-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="66567-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="66567-113">See Also</span></span>

- [<span data-ttu-id="66567-114">Microsoft. Quantum. Canon. RestrictedToSubregister</span><span class="sxs-lookup"><span data-stu-id="66567-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)