---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexC
title: Operação ApplyToEachIndexC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexC
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 387d7ea24b9251386a71b42a1f51ce70933bf6fc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694202"
---
# <a name="applytoeachindexc-operation"></a><span data-ttu-id="1baf3-102">Operação ApplyToEachIndexC</span><span class="sxs-lookup"><span data-stu-id="1baf3-102">ApplyToEachIndexC operation</span></span>

<span data-ttu-id="1baf3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1baf3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1baf3-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1baf3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1baf3-105">Aplica uma operação single-qubit para cada elemento indexado em um registro.</span><span class="sxs-lookup"><span data-stu-id="1baf3-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="1baf3-106">O modificador `C` indica que a operação de qubit única é controlável.</span><span class="sxs-lookup"><span data-stu-id="1baf3-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachIndexC<'T> (singleElementOperation : ((Int, 'T) => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="1baf3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1baf3-107">Input</span></span>

### <a name="singleelementoperation--intt--unit-ctl"></a><span data-ttu-id="1baf3-108">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1baf3-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="1baf3-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="1baf3-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="1baf3-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="1baf3-110">register : 'T[]</span></span>

<span data-ttu-id="1baf3-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="1baf3-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1baf3-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1baf3-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1baf3-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="1baf3-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1baf3-114">T'</span><span class="sxs-lookup"><span data-stu-id="1baf3-114">'T</span></span>

<span data-ttu-id="1baf3-115">O destino no qual cada uma das operações atua.</span><span class="sxs-lookup"><span data-stu-id="1baf3-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="1baf3-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1baf3-116">See Also</span></span>

- [<span data-ttu-id="1baf3-117">Microsoft. Quantum. Canon. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="1baf3-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)