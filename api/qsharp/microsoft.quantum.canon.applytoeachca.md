---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Operação ApplyToEachCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: b24fbb8c7a1a55c0a7750c5d096a61f4824dadfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694205"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="f298f-102">Operação ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="f298f-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="f298f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f298f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f298f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f298f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f298f-105">Aplica uma operação de qubit único a cada elemento em um registro.</span><span class="sxs-lookup"><span data-stu-id="f298f-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="f298f-106">O modificador `CA` indica que a operação single-qubit é controlável e adjointable.</span><span class="sxs-lookup"><span data-stu-id="f298f-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f298f-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f298f-107">Input</span></span>

### <a name="singleelementoperation--t--unit-adj--ctl"></a><span data-ttu-id="f298f-108">singleElementOperation: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="f298f-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="f298f-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="f298f-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="f298f-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="f298f-110">register : 'T[]</span></span>

<span data-ttu-id="f298f-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="f298f-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f298f-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f298f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f298f-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f298f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f298f-114">T'</span><span class="sxs-lookup"><span data-stu-id="f298f-114">'T</span></span>

<span data-ttu-id="f298f-115">O destino no qual a operação atua.</span><span class="sxs-lookup"><span data-stu-id="f298f-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="f298f-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f298f-116">See Also</span></span>

- [<span data-ttu-id="f298f-117">Microsoft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="f298f-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)