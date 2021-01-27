---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubits
title: Operação ApplyToFirstTwoQubits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubits
qsharp.summary: Applies an operation to the first two qubits in the register.
ms.openlocfilehash: c89ea89c055a950a9aee533653d40c84d8e179da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841358"
---
# <a name="applytofirsttwoqubits-operation"></a><span data-ttu-id="21192-102">Operação ApplyToFirstTwoQubits</span><span class="sxs-lookup"><span data-stu-id="21192-102">ApplyToFirstTwoQubits operation</span></span>

<span data-ttu-id="21192-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="21192-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="21192-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="21192-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="21192-105">Aplica uma operação às duas primeiras qubits no registro.</span><span class="sxs-lookup"><span data-stu-id="21192-105">Applies an operation to the first two qubits in the register.</span></span>

```qsharp
operation ApplyToFirstTwoQubits (op : ((Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="21192-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="21192-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="21192-107">op: ([qubit](xref:microsoft.quantum.lang-ref.qubit),[qubit](xref:microsoft.quantum.lang-ref.qubit)) = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="21192-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="21192-108">Uma operação a ser aplicada às duas primeiras qubits</span><span class="sxs-lookup"><span data-stu-id="21192-108">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="21192-109">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="21192-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="21192-110">Matriz qubit para as duas primeiras qubits das quais a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="21192-110">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="21192-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="21192-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="21192-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="21192-112">Remarks</span></span>

<span data-ttu-id="21192-113">Isso é equivalente a:</span><span class="sxs-lookup"><span data-stu-id="21192-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="21192-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="21192-114">See Also</span></span>

- [<span data-ttu-id="21192-115">Microsoft. Quantum. Canon. ApplyToFirstTwoQubitsA</span><span class="sxs-lookup"><span data-stu-id="21192-115">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA)
- [<span data-ttu-id="21192-116">Microsoft. Quantum. Canon. ApplyToFirstTwoQubitsC</span><span class="sxs-lookup"><span data-stu-id="21192-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC)
- [<span data-ttu-id="21192-117">Microsoft. Quantum. Canon. ApplyToFirstTwoQubitsCA</span><span class="sxs-lookup"><span data-stu-id="21192-117">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA)