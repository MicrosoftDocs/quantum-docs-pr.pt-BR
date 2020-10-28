---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC
title: Operação ApplyToFirstTwoQubitsC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsC
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 97706ffcc8700a0055ff37bbbaccc6fb4f8854b6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694167"
---
# <a name="applytofirsttwoqubitsc-operation"></a><span data-ttu-id="4ac4c-102">Operação ApplyToFirstTwoQubitsC</span><span class="sxs-lookup"><span data-stu-id="4ac4c-102">ApplyToFirstTwoQubitsC operation</span></span>

<span data-ttu-id="4ac4c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4ac4c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4ac4c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4ac4c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4ac4c-105">Aplica uma operação às duas primeiras qubits no registro.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="4ac4c-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsC (op : ((Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4ac4c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ac4c-107">Input</span></span>

### <a name="op--qubitqubit--unit-ctl"></a><span data-ttu-id="4ac4c-108">op: ([qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4ac4c-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="4ac4c-109">Uma operação a ser aplicada às duas primeiras qubits</span><span class="sxs-lookup"><span data-stu-id="4ac4c-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="4ac4c-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4ac4c-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="4ac4c-111">Matriz qubit para as duas primeiras qubits das quais a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4ac4c-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4ac4c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4ac4c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ac4c-113">Remarks</span></span>

<span data-ttu-id="4ac4c-114">Isso é equivalente a:</span><span class="sxs-lookup"><span data-stu-id="4ac4c-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="4ac4c-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4ac4c-115">See Also</span></span>

- [<span data-ttu-id="4ac4c-116">Microsoft. Quantum. Canon. ApplyToFirstTwoQubits</span><span class="sxs-lookup"><span data-stu-id="4ac4c-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)