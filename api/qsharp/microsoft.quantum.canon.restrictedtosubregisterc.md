---
uid: Microsoft.Quantum.Canon.RestrictedToSubregisterC
title: Função RestrictedToSubregisterC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RestrictedToSubregisterC
qsharp.summary: Restricts an operation to an array of indices of a register, i.e., a subregister. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: f44e9ea4d17dcadc6d3c64941529db819b7f9784
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840217"
---
# <a name="restrictedtosubregisterc-function"></a><span data-ttu-id="995e0-102">Função RestrictedToSubregisterC</span><span class="sxs-lookup"><span data-stu-id="995e0-102">RestrictedToSubregisterC function</span></span>

<span data-ttu-id="995e0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="995e0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="995e0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="995e0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="995e0-105">Restringe uma operação a uma matriz de índices de um registro, ou seja, um subregistro.</span><span class="sxs-lookup"><span data-stu-id="995e0-105">Restricts an operation to an array of indices of a register, i.e., a subregister.</span></span>
<span data-ttu-id="995e0-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="995e0-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
function RestrictedToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[]) : (Qubit[] => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="995e0-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="995e0-107">Input</span></span>

### <a name="op--qubit--unit--is-ctl"></a><span data-ttu-id="995e0-108">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="995e0-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="995e0-109">Operação a ser restrita a um subregistro.</span><span class="sxs-lookup"><span data-stu-id="995e0-109">Operation to be restricted to a subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="995e0-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="995e0-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="995e0-111">Matriz de índices, indicando a qual qubits a operação será restrita.</span><span class="sxs-lookup"><span data-stu-id="995e0-111">Array of indices, indicating to which qubits the operation will be restricted.</span></span>



## <a name="output--qubit--unit--is-ctl"></a><span data-ttu-id="995e0-112">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL</span><span class="sxs-lookup"><span data-stu-id="995e0-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="995e0-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="995e0-113">See Also</span></span>

- [<span data-ttu-id="995e0-114">Microsoft. Quantum. Canon. RestrictedToSubregister</span><span class="sxs-lookup"><span data-stu-id="995e0-114">Microsoft.Quantum.Canon.RestrictedToSubregister</span></span>](xref:Microsoft.Quantum.Canon.RestrictedToSubregister)