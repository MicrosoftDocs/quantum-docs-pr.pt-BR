---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Operação ApplyToFirstQubitA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 00dbff0b562f90653c8569589e838f11e6c938e8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694184"
---
# <a name="applytofirstqubita-operation"></a><span data-ttu-id="c3ea6-102">Operação ApplyToFirstQubitA</span><span class="sxs-lookup"><span data-stu-id="c3ea6-102">ApplyToFirstQubitA operation</span></span>

<span data-ttu-id="c3ea6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c3ea6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c3ea6-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c3ea6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c3ea6-105">Aplica uma operação ao primeiro qubit no registro.</span><span class="sxs-lookup"><span data-stu-id="c3ea6-105">Applies an operation to the first qubit in the register.</span></span>
<span data-ttu-id="c3ea6-106">O modificador `A` indica que a operação é de adjointable.</span><span class="sxs-lookup"><span data-stu-id="c3ea6-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c3ea6-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3ea6-107">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="c3ea6-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit) => adj da [unidade](xref:microsoft.quantum.lang-ref.unit) qubit</span><span class="sxs-lookup"><span data-stu-id="c3ea6-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="c3ea6-109">Uma operação a ser aplicada ao primeiro qubit</span><span class="sxs-lookup"><span data-stu-id="c3ea6-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="c3ea6-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c3ea6-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c3ea6-111">Matriz qubit para a primeira qubit da qual a operação é aplicada</span><span class="sxs-lookup"><span data-stu-id="c3ea6-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="c3ea6-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c3ea6-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="c3ea6-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c3ea6-113">See Also</span></span>

- [<span data-ttu-id="c3ea6-114">Microsoft. Quantum. Canon. ApplyToFirstQubit</span><span class="sxs-lookup"><span data-stu-id="c3ea6-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)