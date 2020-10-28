---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitCA
title: Operação ApplyToFirstQubitCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitCA
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 2e1db23ad819a85df99a826f406d9b0fbcc7a175
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694183"
---
# <a name="applytofirstqubitca-operation"></a><span data-ttu-id="49a24-102">Operação ApplyToFirstQubitCA</span><span class="sxs-lookup"><span data-stu-id="49a24-102">ApplyToFirstQubitCA operation</span></span>

<span data-ttu-id="49a24-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="49a24-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="49a24-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="49a24-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="49a24-105">Aplica a operação op para o primeiro qubit no registro.</span><span class="sxs-lookup"><span data-stu-id="49a24-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="49a24-106">O modificador `CA` indica que a operação é controlável e de adjointable.</span><span class="sxs-lookup"><span data-stu-id="49a24-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitCA (op : (Qubit => Unit is Adj + Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="49a24-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="49a24-107">Input</span></span>

### <a name="op--qubit--unit-adj--ctl"></a><span data-ttu-id="49a24-108">op: [qubit](xref:microsoft.quantum.lang-ref.qubit) da => [unidade de comutação](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="49a24-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="49a24-109">Uma operação a ser aplicada ao primeiro qubit</span><span class="sxs-lookup"><span data-stu-id="49a24-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="49a24-110">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="49a24-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="49a24-111">Matriz qubit para a primeira qubit da qual a operação é aplicada</span><span class="sxs-lookup"><span data-stu-id="49a24-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="49a24-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="49a24-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="49a24-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="49a24-113">See Also</span></span>

- [<span data-ttu-id="49a24-114">Microsoft. Quantum. Canon. ApplyToFirstQubit</span><span class="sxs-lookup"><span data-stu-id="49a24-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)