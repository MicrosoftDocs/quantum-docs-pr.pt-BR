---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitC
title: Operação ApplyToFirstQubitC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitC
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: e2c137ad4a8252731acf94d6f2343f8fd386b8e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694185"
---
# <a name="applytofirstqubitc-operation"></a><span data-ttu-id="73ca8-102">Operação ApplyToFirstQubitC</span><span class="sxs-lookup"><span data-stu-id="73ca8-102">ApplyToFirstQubitC operation</span></span>

<span data-ttu-id="73ca8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="73ca8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="73ca8-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="73ca8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="73ca8-105">Aplica a operação op para o primeiro qubit no registro.</span><span class="sxs-lookup"><span data-stu-id="73ca8-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="73ca8-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="73ca8-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstQubitC (op : (Qubit => Unit is Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="73ca8-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="73ca8-107">Input</span></span>

### <a name="op--qubit--unit-ctl"></a><span data-ttu-id="73ca8-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) qubit</span><span class="sxs-lookup"><span data-stu-id="73ca8-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="73ca8-109">Uma operação a ser aplicada ao primeiro qubit</span><span class="sxs-lookup"><span data-stu-id="73ca8-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="73ca8-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="73ca8-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="73ca8-111">Matriz qubit para a primeira qubit da qual a operação é aplicada</span><span class="sxs-lookup"><span data-stu-id="73ca8-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="73ca8-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="73ca8-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="73ca8-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="73ca8-113">See Also</span></span>

- [<span data-ttu-id="73ca8-114">Microsoft. Quantum. Canon. ApplyToFirstQubit</span><span class="sxs-lookup"><span data-stu-id="73ca8-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)