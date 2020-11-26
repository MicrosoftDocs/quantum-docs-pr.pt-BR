---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Operação ApplyToEachC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 535f815503e20b5cee35f3f273a714203a4baf12
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217774"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="faefe-102">Operação ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="faefe-102">ApplyToEachC operation</span></span>

<span data-ttu-id="faefe-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="faefe-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="faefe-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="faefe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="faefe-105">Aplica uma operação de qubit único a cada elemento em um registro.</span><span class="sxs-lookup"><span data-stu-id="faefe-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="faefe-106">O modificador `C` indica que a operação de qubit única é controlável.</span><span class="sxs-lookup"><span data-stu-id="faefe-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="faefe-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="faefe-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-ctl"></a><span data-ttu-id="faefe-108">singleElementOperation: T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="faefe-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="faefe-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="faefe-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="faefe-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="faefe-110">register : 'T[]</span></span>

<span data-ttu-id="faefe-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="faefe-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="faefe-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="faefe-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="faefe-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="faefe-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="faefe-114">T'</span><span class="sxs-lookup"><span data-stu-id="faefe-114">'T</span></span>

<span data-ttu-id="faefe-115">O destino no qual a operação atua.</span><span class="sxs-lookup"><span data-stu-id="faefe-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="faefe-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="faefe-116">See Also</span></span>

- [<span data-ttu-id="faefe-117">Microsoft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="faefe-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)