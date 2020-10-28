---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Operação ApplyToEachA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 9485c6549ed4e1a6fb3abdfa3f85ba35579d8b0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694209"
---
# <a name="applytoeacha-operation"></a><span data-ttu-id="864e8-102">Operação ApplyToEachA</span><span class="sxs-lookup"><span data-stu-id="864e8-102">ApplyToEachA operation</span></span>

<span data-ttu-id="864e8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="864e8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="864e8-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="864e8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="864e8-105">Aplica uma operação de qubit único a cada elemento em um registro.</span><span class="sxs-lookup"><span data-stu-id="864e8-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="864e8-106">O modificador `A` indica que a operação single-qubit é o adjointable.</span><span class="sxs-lookup"><span data-stu-id="864e8-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="864e8-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="864e8-107">Input</span></span>

### <a name="singleelementoperation--t--unit-adj"></a><span data-ttu-id="864e8-108">singleElementOperation: t => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="864e8-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="864e8-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="864e8-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="864e8-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="864e8-110">register : 'T[]</span></span>

<span data-ttu-id="864e8-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="864e8-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="864e8-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="864e8-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="864e8-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="864e8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="864e8-114">T'</span><span class="sxs-lookup"><span data-stu-id="864e8-114">'T</span></span>

<span data-ttu-id="864e8-115">O destino no qual a operação atua.</span><span class="sxs-lookup"><span data-stu-id="864e8-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="864e8-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="864e8-116">See Also</span></span>

- [<span data-ttu-id="864e8-117">Microsoft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="864e8-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)