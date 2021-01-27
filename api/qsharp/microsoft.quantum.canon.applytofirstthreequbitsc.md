---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC
title: Operação ApplyToFirstThreeQubitsC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsC
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2c4fe7c645913cb0703982d78f65645f141fdcae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841397"
---
# <a name="applytofirstthreequbitsc-operation"></a><span data-ttu-id="087d6-102">Operação ApplyToFirstThreeQubitsC</span><span class="sxs-lookup"><span data-stu-id="087d6-102">ApplyToFirstThreeQubitsC operation</span></span>

<span data-ttu-id="087d6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="087d6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="087d6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="087d6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="087d6-105">Aplica uma operação às três primeiras qubits no registro.</span><span class="sxs-lookup"><span data-stu-id="087d6-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="087d6-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="087d6-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsC (op : ((Qubit, Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="087d6-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="087d6-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit--is-ctl"></a><span data-ttu-id="087d6-108">op: ([qubit](xref:microsoft.quantum.lang-ref.qubit),[qubit](xref:microsoft.quantum.lang-ref.qubit),[qubit](xref:microsoft.quantum.lang-ref.qubit)) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL</span><span class="sxs-lookup"><span data-stu-id="087d6-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="087d6-109">Uma operação a ser aplicada aos três primeiros qubits</span><span class="sxs-lookup"><span data-stu-id="087d6-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="087d6-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="087d6-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="087d6-111">Matriz qubit para os três primeiros qubits dos quais a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="087d6-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="087d6-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="087d6-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="087d6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="087d6-113">Remarks</span></span>

<span data-ttu-id="087d6-114">Isso é equivalente a:</span><span class="sxs-lookup"><span data-stu-id="087d6-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="087d6-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="087d6-115">See Also</span></span>

- [<span data-ttu-id="087d6-116">Microsoft. Quantum. Canon. ApplyToFirstThreeQubits</span><span class="sxs-lookup"><span data-stu-id="087d6-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)