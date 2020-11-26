---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Operação ApplyToEachA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 9819e78760caf6180edc5c2ca5e402060e3029a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217791"
---
# <a name="applytoeacha-operation"></a><span data-ttu-id="26b28-102">Operação ApplyToEachA</span><span class="sxs-lookup"><span data-stu-id="26b28-102">ApplyToEachA operation</span></span>

<span data-ttu-id="26b28-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="26b28-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="26b28-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="26b28-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="26b28-105">Aplica uma operação de qubit único a cada elemento em um registro.</span><span class="sxs-lookup"><span data-stu-id="26b28-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="26b28-106">O modificador `A` indica que a operação single-qubit é o adjointable.</span><span class="sxs-lookup"><span data-stu-id="26b28-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="26b28-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="26b28-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj"></a><span data-ttu-id="26b28-108">singleElementOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="26b28-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="26b28-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="26b28-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="26b28-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="26b28-110">register : 'T[]</span></span>

<span data-ttu-id="26b28-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="26b28-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="26b28-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="26b28-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="26b28-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="26b28-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="26b28-114">T'</span><span class="sxs-lookup"><span data-stu-id="26b28-114">'T</span></span>

<span data-ttu-id="26b28-115">O destino no qual a operação atua.</span><span class="sxs-lookup"><span data-stu-id="26b28-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="26b28-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="26b28-116">See Also</span></span>

- [<span data-ttu-id="26b28-117">Microsoft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="26b28-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)