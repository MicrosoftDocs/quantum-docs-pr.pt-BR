---
uid: Microsoft.Quantum.Canon.ApplyWithC
title: Operação ApplyWithC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithC
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: 8de1ddf0bf176853b33926be7647bc5d1d35095d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694112"
---
# <a name="applywithc-operation"></a><span data-ttu-id="82fc9-102">Operação ApplyWithC</span><span class="sxs-lookup"><span data-stu-id="82fc9-102">ApplyWithC operation</span></span>

<span data-ttu-id="82fc9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="82fc9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="82fc9-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="82fc9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="82fc9-105">Dadas duas operações, o aplica-se uma como conjugado com a outra.</span><span class="sxs-lookup"><span data-stu-id="82fc9-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithC<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Ctl), target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="82fc9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="82fc9-106">Description</span></span>

<span data-ttu-id="82fc9-107">Dadas duas operações, respectivamente descritas por operadores unitários $U $ e $V $, aplica-as na sequência $U ^ {\dagger} V U $.</span><span class="sxs-lookup"><span data-stu-id="82fc9-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="82fc9-108">Ou seja, essa operação implementa o operador unitário fornecido por $V $ conjugado com $U $.</span><span class="sxs-lookup"><span data-stu-id="82fc9-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="82fc9-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="82fc9-109">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="82fc9-110">outerOperation: t => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82fc9-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="82fc9-111">A operação $U $ que deve ser usada para conjugar $V $.</span><span class="sxs-lookup"><span data-stu-id="82fc9-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="82fc9-112">Observe que a operação externa $U $ precisa ser adjointable, mas não precisa ser controlável.</span><span class="sxs-lookup"><span data-stu-id="82fc9-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit-ctl"></a><span data-ttu-id="82fc9-113">innerOperation: t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82fc9-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="82fc9-114">A operação $V $ sendo conjugada.</span><span class="sxs-lookup"><span data-stu-id="82fc9-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="82fc9-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="82fc9-115">target : 'T</span></span>

<span data-ttu-id="82fc9-116">A entrada a ser fornecida para as operações externas e internas.</span><span class="sxs-lookup"><span data-stu-id="82fc9-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="82fc9-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82fc9-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="82fc9-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="82fc9-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="82fc9-119">T'</span><span class="sxs-lookup"><span data-stu-id="82fc9-119">'T</span></span>

<span data-ttu-id="82fc9-120">O destino no qual cada uma das operações internas e externas atuam.</span><span class="sxs-lookup"><span data-stu-id="82fc9-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="82fc9-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="82fc9-121">Remarks</span></span>

<span data-ttu-id="82fc9-122">A operação externa sempre é presumida como adjointable, mas não precisa ser controlável para que a operação combinada seja controlável.</span><span class="sxs-lookup"><span data-stu-id="82fc9-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="82fc9-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="82fc9-123">See Also</span></span>

- [<span data-ttu-id="82fc9-124">Microsoft. Quantum. Canon. ApplyWith</span><span class="sxs-lookup"><span data-stu-id="82fc9-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="82fc9-125">Microsoft. Quantum. Canon. ApplyWithA</span><span class="sxs-lookup"><span data-stu-id="82fc9-125">Microsoft.Quantum.Canon.ApplyWithA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [<span data-ttu-id="82fc9-126">Microsoft. Quantum. Canon. ApplyWithCA</span><span class="sxs-lookup"><span data-stu-id="82fc9-126">Microsoft.Quantum.Canon.ApplyWithCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithCA)