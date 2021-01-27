---
uid: Microsoft.Quantum.Canon.ApplyWithA
title: Operação ApplyWithA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: f717347a81e4efa5ad1736485ad9e1c518d736a7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841169"
---
# <a name="applywitha-operation"></a><span data-ttu-id="d921f-102">Operação ApplyWithA</span><span class="sxs-lookup"><span data-stu-id="d921f-102">ApplyWithA operation</span></span>

<span data-ttu-id="d921f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d921f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d921f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d921f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d921f-105">Dadas duas operações, o aplica-se uma como conjugado com a outra.</span><span class="sxs-lookup"><span data-stu-id="d921f-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj), target : 'T) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="d921f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d921f-106">Description</span></span>

<span data-ttu-id="d921f-107">Dadas duas operações, respectivamente descritas por operadores unitários $U $ e $V $, aplica-as na sequência $U ^ {\dagger} V U $.</span><span class="sxs-lookup"><span data-stu-id="d921f-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="d921f-108">Ou seja, essa operação implementa o operador unitário fornecido por $V $ conjugado com $U $.</span><span class="sxs-lookup"><span data-stu-id="d921f-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="d921f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="d921f-109">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="d921f-110">outerOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="d921f-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d921f-111">A operação $U $ que deve ser usada para conjugar $V $.</span><span class="sxs-lookup"><span data-stu-id="d921f-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="d921f-112">Observe que a operação externa $U $ precisa ser adjointable, mas não precisa ser controlável.</span><span class="sxs-lookup"><span data-stu-id="d921f-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj"></a><span data-ttu-id="d921f-113">innerOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="d921f-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d921f-114">A operação $V $ sendo conjugada.</span><span class="sxs-lookup"><span data-stu-id="d921f-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="d921f-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="d921f-115">target : 'T</span></span>

<span data-ttu-id="d921f-116">A entrada a ser fornecida para as operações externas e internas.</span><span class="sxs-lookup"><span data-stu-id="d921f-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d921f-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d921f-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d921f-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d921f-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d921f-119">T'</span><span class="sxs-lookup"><span data-stu-id="d921f-119">'T</span></span>

<span data-ttu-id="d921f-120">O destino no qual cada uma das operações internas e externas atuam.</span><span class="sxs-lookup"><span data-stu-id="d921f-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="d921f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d921f-121">Remarks</span></span>

<span data-ttu-id="d921f-122">A operação externa sempre é presumida como adjointable, mas não precisa ser controlável para que a operação combinada seja controlável.</span><span class="sxs-lookup"><span data-stu-id="d921f-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="d921f-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d921f-123">See Also</span></span>

- [<span data-ttu-id="d921f-124">Microsoft. Quantum. Canon. ApplyWith</span><span class="sxs-lookup"><span data-stu-id="d921f-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="d921f-125">Microsoft. Quantum. Canon. ApplyWithC</span><span class="sxs-lookup"><span data-stu-id="d921f-125">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)
- [<span data-ttu-id="d921f-126">Microsoft. Quantum. Canon. ApplyWithCA</span><span class="sxs-lookup"><span data-stu-id="d921f-126">Microsoft.Quantum.Canon.ApplyWithCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithCA)