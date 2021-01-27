---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitC
title: Operação ApplyToFirstQubitC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitC
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: a36d20e03ebed82435d1d4136f4ce777eb468926
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850710"
---
# <a name="applytofirstqubitc-operation"></a><span data-ttu-id="ccb5a-102">Operação ApplyToFirstQubitC</span><span class="sxs-lookup"><span data-stu-id="ccb5a-102">ApplyToFirstQubitC operation</span></span>

<span data-ttu-id="ccb5a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ccb5a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ccb5a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ccb5a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ccb5a-105">Aplica a operação op para o primeiro qubit no registro.</span><span class="sxs-lookup"><span data-stu-id="ccb5a-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="ccb5a-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="ccb5a-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstQubitC (op : (Qubit => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="ccb5a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ccb5a-107">Input</span></span>

### <a name="op--qubit--unit--is-ctl"></a><span data-ttu-id="ccb5a-108">op: [](xref:microsoft.quantum.lang-ref.qubit) a => [unidade](xref:microsoft.quantum.lang-ref.unit) qubit é CTL</span><span class="sxs-lookup"><span data-stu-id="ccb5a-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="ccb5a-109">Uma operação a ser aplicada ao primeiro qubit</span><span class="sxs-lookup"><span data-stu-id="ccb5a-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="ccb5a-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ccb5a-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ccb5a-111">Matriz qubit para a primeira qubit da qual a operação é aplicada</span><span class="sxs-lookup"><span data-stu-id="ccb5a-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="ccb5a-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ccb5a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="ccb5a-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ccb5a-113">See Also</span></span>

- [<span data-ttu-id="ccb5a-114">Microsoft. Quantum. Canon. ApplyToFirstQubit</span><span class="sxs-lookup"><span data-stu-id="ccb5a-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)