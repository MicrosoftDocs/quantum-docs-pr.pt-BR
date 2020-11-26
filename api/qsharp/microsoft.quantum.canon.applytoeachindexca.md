---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Operação ApplyToEachIndexCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: abb616498a8ff9c3348df81cf0ca1a1669561eec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208934"
---
# <a name="applytoeachindexca-operation"></a><span data-ttu-id="ec8bb-102">Operação ApplyToEachIndexCA</span><span class="sxs-lookup"><span data-stu-id="ec8bb-102">ApplyToEachIndexCA operation</span></span>

<span data-ttu-id="ec8bb-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ec8bb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ec8bb-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ec8bb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ec8bb-105">Aplica uma operação single-qubit para cada elemento indexado em um registro.</span><span class="sxs-lookup"><span data-stu-id="ec8bb-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="ec8bb-106">O modificador `CA` indica que a operação single-qubit é jointable e controlável.</span><span class="sxs-lookup"><span data-stu-id="ec8bb-106">The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.</span></span>

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ec8bb-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec8bb-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj--ctl"></a><span data-ttu-id="ec8bb-108">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="ec8bb-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ec8bb-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="ec8bb-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="ec8bb-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="ec8bb-110">register : 'T[]</span></span>

<span data-ttu-id="ec8bb-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="ec8bb-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ec8bb-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec8bb-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ec8bb-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ec8bb-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ec8bb-114">T'</span><span class="sxs-lookup"><span data-stu-id="ec8bb-114">'T</span></span>

<span data-ttu-id="ec8bb-115">O destino no qual cada uma das operações atua.</span><span class="sxs-lookup"><span data-stu-id="ec8bb-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec8bb-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ec8bb-116">See Also</span></span>

- [<span data-ttu-id="ec8bb-117">Microsoft. Quantum. Canon. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="ec8bb-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)