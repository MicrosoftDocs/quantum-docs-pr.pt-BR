---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC
title: Operação ApplyToFirstTwoQubitsC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsC
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: f71209a806b0d1d712a3c776eb45e62d1cd5d5f7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841344"
---
# <a name="applytofirsttwoqubitsc-operation"></a><span data-ttu-id="85466-102">Operação ApplyToFirstTwoQubitsC</span><span class="sxs-lookup"><span data-stu-id="85466-102">ApplyToFirstTwoQubitsC operation</span></span>

<span data-ttu-id="85466-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="85466-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="85466-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85466-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85466-105">Aplica uma operação às duas primeiras qubits no registro.</span><span class="sxs-lookup"><span data-stu-id="85466-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="85466-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="85466-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsC (op : ((Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="85466-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="85466-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-ctl"></a><span data-ttu-id="85466-108">op: ([qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL</span><span class="sxs-lookup"><span data-stu-id="85466-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="85466-109">Uma operação a ser aplicada às duas primeiras qubits</span><span class="sxs-lookup"><span data-stu-id="85466-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="85466-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="85466-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="85466-111">Matriz qubit para as duas primeiras qubits das quais a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="85466-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="85466-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="85466-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="85466-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="85466-113">Remarks</span></span>

<span data-ttu-id="85466-114">Isso é equivalente a:</span><span class="sxs-lookup"><span data-stu-id="85466-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="85466-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="85466-115">See Also</span></span>

- [<span data-ttu-id="85466-116">Microsoft. Quantum. Canon. ApplyToFirstTwoQubits</span><span class="sxs-lookup"><span data-stu-id="85466-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)