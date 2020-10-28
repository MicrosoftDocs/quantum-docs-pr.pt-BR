---
uid: Microsoft.Quantum.Canon.ApplyWithCA
title: Operação ApplyWithCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithCA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: abc62791416e78c1b2937a226327b71da8b8e288
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694110"
---
# <a name="applywithca-operation"></a><span data-ttu-id="c7454-102">Operação ApplyWithCA</span><span class="sxs-lookup"><span data-stu-id="c7454-102">ApplyWithCA operation</span></span>

<span data-ttu-id="c7454-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c7454-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c7454-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c7454-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c7454-105">Dadas duas operações, o aplica-se uma como conjugado com a outra.</span><span class="sxs-lookup"><span data-stu-id="c7454-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl), target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="c7454-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7454-106">Description</span></span>

<span data-ttu-id="c7454-107">Dadas duas operações, respectivamente descritas por operadores unitários $U $ e $V $, aplica-as na sequência $U ^ {\dagger} V U $.</span><span class="sxs-lookup"><span data-stu-id="c7454-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="c7454-108">Ou seja, essa operação implementa o operador unitário fornecido por $V $ conjugado com $U $.</span><span class="sxs-lookup"><span data-stu-id="c7454-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="c7454-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7454-109">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="c7454-110">outerOperation: t => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7454-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="c7454-111">A operação $U $ que deve ser usada para conjugar $V $.</span><span class="sxs-lookup"><span data-stu-id="c7454-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="c7454-112">Observe que a operação externa $U $ precisa ser adjointable, mas não precisa ser controlável.</span><span class="sxs-lookup"><span data-stu-id="c7454-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit-adj--ctl"></a><span data-ttu-id="c7454-113">innerOperation: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="c7454-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="c7454-114">A operação $V $ sendo conjugada.</span><span class="sxs-lookup"><span data-stu-id="c7454-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="c7454-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="c7454-115">target : 'T</span></span>

<span data-ttu-id="c7454-116">A entrada a ser fornecida para as operações externas e internas.</span><span class="sxs-lookup"><span data-stu-id="c7454-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c7454-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7454-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c7454-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="c7454-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c7454-119">T'</span><span class="sxs-lookup"><span data-stu-id="c7454-119">'T</span></span>

<span data-ttu-id="c7454-120">O destino no qual cada uma das operações internas e externas atuam.</span><span class="sxs-lookup"><span data-stu-id="c7454-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7454-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7454-121">Remarks</span></span>

<span data-ttu-id="c7454-122">A operação externa sempre é presumida como adjointable, mas não precisa ser controlável para que a operação combinada seja controlável.</span><span class="sxs-lookup"><span data-stu-id="c7454-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7454-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c7454-123">See Also</span></span>

- [<span data-ttu-id="c7454-124">Microsoft. Quantum. Canon. ApplyWith</span><span class="sxs-lookup"><span data-stu-id="c7454-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="c7454-125">Microsoft. Quantum. Canon. ApplyWithA</span><span class="sxs-lookup"><span data-stu-id="c7454-125">Microsoft.Quantum.Canon.ApplyWithA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [<span data-ttu-id="c7454-126">Microsoft. Quantum. Canon. ApplyWithC</span><span class="sxs-lookup"><span data-stu-id="c7454-126">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)