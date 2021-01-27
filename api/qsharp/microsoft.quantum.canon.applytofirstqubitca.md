---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitCA
title: Operação ApplyToFirstQubitCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitCA
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: ba82199cc7a548d771027141780873c05de71c57
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841440"
---
# <a name="applytofirstqubitca-operation"></a><span data-ttu-id="bca68-102">Operação ApplyToFirstQubitCA</span><span class="sxs-lookup"><span data-stu-id="bca68-102">ApplyToFirstQubitCA operation</span></span>

<span data-ttu-id="bca68-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bca68-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bca68-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bca68-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bca68-105">Aplica a operação op para o primeiro qubit no registro.</span><span class="sxs-lookup"><span data-stu-id="bca68-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="bca68-106">O modificador `CA` indica que a operação é controlável e de adjointable.</span><span class="sxs-lookup"><span data-stu-id="bca68-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitCA (op : (Qubit => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="bca68-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bca68-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="bca68-108">op: [](xref:microsoft.quantum.lang-ref.qubit) a => [unidade](xref:microsoft.quantum.lang-ref.unit) qubit é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="bca68-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="bca68-109">Uma operação a ser aplicada ao primeiro qubit</span><span class="sxs-lookup"><span data-stu-id="bca68-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="bca68-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bca68-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bca68-111">Matriz qubit para a primeira qubit da qual a operação é aplicada</span><span class="sxs-lookup"><span data-stu-id="bca68-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="bca68-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bca68-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="bca68-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bca68-113">See Also</span></span>

- [<span data-ttu-id="bca68-114">Microsoft. Quantum. Canon. ApplyToFirstQubit</span><span class="sxs-lookup"><span data-stu-id="bca68-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)