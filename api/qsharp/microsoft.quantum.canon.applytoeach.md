---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Operação ApplyToEach
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: e1625829e2e9efd9d39fe0692f01c1cbbffc651c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694211"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="efaf5-102">Operação ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="efaf5-102">ApplyToEach operation</span></span>

<span data-ttu-id="efaf5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="efaf5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="efaf5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="efaf5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="efaf5-105">Aplica uma operação de qubit único a cada elemento em um registro.</span><span class="sxs-lookup"><span data-stu-id="efaf5-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="efaf5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="efaf5-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="efaf5-107">singleElementOperation: t = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="efaf5-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="efaf5-108">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="efaf5-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="efaf5-109">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="efaf5-109">register : 'T[]</span></span>

<span data-ttu-id="efaf5-110">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="efaf5-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="efaf5-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="efaf5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="efaf5-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="efaf5-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="efaf5-113">T'</span><span class="sxs-lookup"><span data-stu-id="efaf5-113">'T</span></span>

<span data-ttu-id="efaf5-114">O destino no qual a operação atua.</span><span class="sxs-lookup"><span data-stu-id="efaf5-114">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="efaf5-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="efaf5-115">See Also</span></span>

- [<span data-ttu-id="efaf5-116">Microsoft. Quantum. Canon. ApplyToEachC</span><span class="sxs-lookup"><span data-stu-id="efaf5-116">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="efaf5-117">Microsoft. Quantum. Canon. ApplyToEachA</span><span class="sxs-lookup"><span data-stu-id="efaf5-117">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="efaf5-118">Microsoft. Quantum. Canon. ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="efaf5-118">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)