---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Operação ApplyToEachCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: dcfd4619a77413e71044e6a7d5fc19a9f22bbf94
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217740"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="d4c0d-102">Operação ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="d4c0d-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="d4c0d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d4c0d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d4c0d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d4c0d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d4c0d-105">Aplica uma operação de qubit único a cada elemento em um registro.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="d4c0d-106">O modificador `CA` indica que a operação single-qubit é controlável e adjointable.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d4c0d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d4c0d-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj--ctl"></a><span data-ttu-id="d4c0d-108">singleElementOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="d4c0d-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="d4c0d-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="d4c0d-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="d4c0d-110">register : 'T[]</span></span>

<span data-ttu-id="d4c0d-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d4c0d-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4c0d-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d4c0d-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d4c0d-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d4c0d-114">T'</span><span class="sxs-lookup"><span data-stu-id="d4c0d-114">'T</span></span>

<span data-ttu-id="d4c0d-115">O destino no qual a operação atua.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4c0d-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d4c0d-116">See Also</span></span>

- [<span data-ttu-id="d4c0d-117">Microsoft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="d4c0d-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)