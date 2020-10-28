---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Operação ApplyToEachIndex
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 4ce184b34add9238e26f9b35b40ec0bddb23ccf9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694204"
---
# <a name="applytoeachindex-operation"></a><span data-ttu-id="e202b-102">Operação ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="e202b-102">ApplyToEachIndex operation</span></span>

<span data-ttu-id="e202b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e202b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e202b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e202b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e202b-105">Aplica uma operação single-qubit para cada elemento indexado em um registro.</span><span class="sxs-lookup"><span data-stu-id="e202b-105">Applies a single-qubit operation to each indexed element in a register.</span></span>

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e202b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e202b-106">Input</span></span>

### <a name="singleelementoperation--intt--unit"></a><span data-ttu-id="e202b-107">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), t) = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="e202b-107">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e202b-108">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="e202b-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="e202b-109">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="e202b-109">register : 'T[]</span></span>

<span data-ttu-id="e202b-110">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="e202b-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e202b-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e202b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e202b-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e202b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e202b-113">T'</span><span class="sxs-lookup"><span data-stu-id="e202b-113">'T</span></span>

<span data-ttu-id="e202b-114">O destino no qual cada uma das operações atua.</span><span class="sxs-lookup"><span data-stu-id="e202b-114">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="e202b-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e202b-115">See Also</span></span>

- [<span data-ttu-id="e202b-116">Microsoft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="e202b-116">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [<span data-ttu-id="e202b-117">Microsoft. Quantum. Canon. ApplyToEachIndexA</span><span class="sxs-lookup"><span data-stu-id="e202b-117">Microsoft.Quantum.Canon.ApplyToEachIndexA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [<span data-ttu-id="e202b-118">Microsoft. Quantum. Canon. ApplyToEachIndexC</span><span class="sxs-lookup"><span data-stu-id="e202b-118">Microsoft.Quantum.Canon.ApplyToEachIndexC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [<span data-ttu-id="e202b-119">Microsoft. Quantum. Canon. ApplyToEachIndexCA</span><span class="sxs-lookup"><span data-stu-id="e202b-119">Microsoft.Quantum.Canon.ApplyToEachIndexCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)