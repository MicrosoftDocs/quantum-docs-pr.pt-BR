---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Operação ApplyToEachC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: dfa18b6eb7a2c42fa2982994a2fc92170b52599c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694207"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="e8246-102">Operação ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="e8246-102">ApplyToEachC operation</span></span>

<span data-ttu-id="e8246-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8246-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8246-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e8246-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e8246-105">Aplica uma operação de qubit único a cada elemento em um registro.</span><span class="sxs-lookup"><span data-stu-id="e8246-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="e8246-106">O modificador `C` indica que a operação de qubit única é controlável.</span><span class="sxs-lookup"><span data-stu-id="e8246-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e8246-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8246-107">Input</span></span>

### <a name="singleelementoperation--t--unit-ctl"></a><span data-ttu-id="e8246-108">singleElementOperation: t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8246-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="e8246-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="e8246-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="e8246-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="e8246-110">register : 'T[]</span></span>

<span data-ttu-id="e8246-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="e8246-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e8246-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8246-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e8246-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e8246-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e8246-114">T'</span><span class="sxs-lookup"><span data-stu-id="e8246-114">'T</span></span>

<span data-ttu-id="e8246-115">O destino no qual a operação atua.</span><span class="sxs-lookup"><span data-stu-id="e8246-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8246-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e8246-116">See Also</span></span>

- [<span data-ttu-id="e8246-117">Microsoft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="e8246-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)