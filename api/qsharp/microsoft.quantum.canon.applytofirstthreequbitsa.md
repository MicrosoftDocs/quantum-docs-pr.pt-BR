---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA
title: Operação ApplyToFirstThreeQubitsA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 502d876df0ed643c40ce6ee48eaf496a90b0f5dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694179"
---
# <a name="applytofirstthreequbitsa-operation"></a><span data-ttu-id="46ee5-102">Operação ApplyToFirstThreeQubitsA</span><span class="sxs-lookup"><span data-stu-id="46ee5-102">ApplyToFirstThreeQubitsA operation</span></span>

<span data-ttu-id="46ee5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="46ee5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="46ee5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="46ee5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="46ee5-105">Aplica uma operação às três primeiras qubits no registro.</span><span class="sxs-lookup"><span data-stu-id="46ee5-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="46ee5-106">O modificador `A` indica que a operação é de adjointable.</span><span class="sxs-lookup"><span data-stu-id="46ee5-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsA (op : ((Qubit, Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="46ee5-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="46ee5-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit-adj"></a><span data-ttu-id="46ee5-108">op: ([qubit](xref:microsoft.quantum.lang-ref.qubit),[qubit](xref:microsoft.quantum.lang-ref.qubit),[qubit](xref:microsoft.quantum.lang-ref.qubit)) => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="46ee5-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="46ee5-109">Uma operação a ser aplicada aos três primeiros qubits</span><span class="sxs-lookup"><span data-stu-id="46ee5-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="46ee5-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="46ee5-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="46ee5-111">Matriz qubit para os três primeiros qubits dos quais a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="46ee5-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="46ee5-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="46ee5-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="46ee5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="46ee5-113">Remarks</span></span>

<span data-ttu-id="46ee5-114">Isso é equivalente a:</span><span class="sxs-lookup"><span data-stu-id="46ee5-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="46ee5-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="46ee5-115">See Also</span></span>

- [<span data-ttu-id="46ee5-116">Microsoft. Quantum. Canon. ApplyToFirstThreeQubits</span><span class="sxs-lookup"><span data-stu-id="46ee5-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)