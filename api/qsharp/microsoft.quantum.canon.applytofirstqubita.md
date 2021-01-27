---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Operação ApplyToFirstQubitA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 2f96c2a8ed31d295bc127c568e0ca24c267638b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841443"
---
# <a name="applytofirstqubita-operation"></a><span data-ttu-id="c4c28-102">Operação ApplyToFirstQubitA</span><span class="sxs-lookup"><span data-stu-id="c4c28-102">ApplyToFirstQubitA operation</span></span>

<span data-ttu-id="c4c28-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c4c28-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c4c28-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c4c28-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c4c28-105">Aplica uma operação ao primeiro qubit no registro.</span><span class="sxs-lookup"><span data-stu-id="c4c28-105">Applies an operation to the first qubit in the register.</span></span>
<span data-ttu-id="c4c28-106">O modificador `A` indica que a operação é de adjointable.</span><span class="sxs-lookup"><span data-stu-id="c4c28-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="c4c28-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4c28-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="c4c28-108">op: [](xref:microsoft.quantum.lang-ref.qubit) a => [unidade](xref:microsoft.quantum.lang-ref.unit) qubit é adj</span><span class="sxs-lookup"><span data-stu-id="c4c28-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c4c28-109">Uma operação a ser aplicada ao primeiro qubit</span><span class="sxs-lookup"><span data-stu-id="c4c28-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="c4c28-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c4c28-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c4c28-111">Matriz qubit para a primeira qubit da qual a operação é aplicada</span><span class="sxs-lookup"><span data-stu-id="c4c28-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="c4c28-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c4c28-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="c4c28-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c4c28-113">See Also</span></span>

- [<span data-ttu-id="c4c28-114">Microsoft. Quantum. Canon. ApplyToFirstQubit</span><span class="sxs-lookup"><span data-stu-id="c4c28-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)