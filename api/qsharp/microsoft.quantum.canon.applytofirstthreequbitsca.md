---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA
title: Operação ApplyToFirstThreeQubitsCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsCA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: bd7a3ac260d370aae9da8691fcd34a8b6221d451
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694176"
---
# <a name="applytofirstthreequbitsca-operation"></a><span data-ttu-id="53f03-102">Operação ApplyToFirstThreeQubitsCA</span><span class="sxs-lookup"><span data-stu-id="53f03-102">ApplyToFirstThreeQubitsCA operation</span></span>

<span data-ttu-id="53f03-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="53f03-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="53f03-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="53f03-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="53f03-105">Aplica uma operação às três primeiras qubits no registro.</span><span class="sxs-lookup"><span data-stu-id="53f03-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="53f03-106">O modificador `CA` indica que a operação é controlável e de adjointable.</span><span class="sxs-lookup"><span data-stu-id="53f03-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsCA (op : ((Qubit, Qubit, Qubit) => Unit is Adj + Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="53f03-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="53f03-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit-adj--ctl"></a><span data-ttu-id="53f03-108">op: ([qubit](xref:microsoft.quantum.lang-ref.qubit),[qubit](xref:microsoft.quantum.lang-ref.qubit),[qubit](xref:microsoft.quantum.lang-ref.qubit)) => [unidade](xref:microsoft.quantum.lang-ref.unit) adj + CTL</span><span class="sxs-lookup"><span data-stu-id="53f03-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="53f03-109">Uma operação a ser aplicada aos três primeiros qubits</span><span class="sxs-lookup"><span data-stu-id="53f03-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="53f03-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="53f03-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="53f03-111">Matriz qubit para os três primeiros qubits dos quais a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="53f03-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="53f03-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="53f03-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="53f03-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="53f03-113">Remarks</span></span>

<span data-ttu-id="53f03-114">Isso é equivalente a:</span><span class="sxs-lookup"><span data-stu-id="53f03-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="53f03-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="53f03-115">See Also</span></span>

- [<span data-ttu-id="53f03-116">Microsoft. Quantum. Canon. ApplyToFirstThreeQubits</span><span class="sxs-lookup"><span data-stu-id="53f03-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)