---
uid: Microsoft.Quantum.Canon.ApplyWithCA
title: Operação ApplyWithCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithCA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: e86c452e9693c5a4d0d4e5a36471ab46bbf66dfe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208135"
---
# <a name="applywithca-operation"></a><span data-ttu-id="4dfb4-102">Operação ApplyWithCA</span><span class="sxs-lookup"><span data-stu-id="4dfb4-102">ApplyWithCA operation</span></span>

<span data-ttu-id="4dfb4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4dfb4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4dfb4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4dfb4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4dfb4-105">Dadas duas operações, o aplica-se uma como conjugado com a outra.</span><span class="sxs-lookup"><span data-stu-id="4dfb4-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl), target : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="4dfb4-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4dfb4-106">Description</span></span>

<span data-ttu-id="4dfb4-107">Dadas duas operações, respectivamente descritas por operadores unitários $U $ e $V $, aplica-as na sequência $U ^ {\dagger} V U $.</span><span class="sxs-lookup"><span data-stu-id="4dfb4-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="4dfb4-108">Ou seja, essa operação implementa o operador unitário fornecido por $V $ conjugado com $U $.</span><span class="sxs-lookup"><span data-stu-id="4dfb4-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="4dfb4-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="4dfb4-109">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="4dfb4-110">outerOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="4dfb4-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="4dfb4-111">A operação $U $ que deve ser usada para conjugar $V $.</span><span class="sxs-lookup"><span data-stu-id="4dfb4-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="4dfb4-112">Observe que a operação externa $U $ precisa ser adjointable, mas não precisa ser controlável.</span><span class="sxs-lookup"><span data-stu-id="4dfb4-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj--ctl"></a><span data-ttu-id="4dfb4-113">innerOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="4dfb4-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="4dfb4-114">A operação $V $ sendo conjugada.</span><span class="sxs-lookup"><span data-stu-id="4dfb4-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="4dfb4-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="4dfb4-115">target : 'T</span></span>

<span data-ttu-id="4dfb4-116">A entrada a ser fornecida para as operações externas e internas.</span><span class="sxs-lookup"><span data-stu-id="4dfb4-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4dfb4-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4dfb4-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4dfb4-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4dfb4-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4dfb4-119">T'</span><span class="sxs-lookup"><span data-stu-id="4dfb4-119">'T</span></span>

<span data-ttu-id="4dfb4-120">O destino no qual cada uma das operações internas e externas atuam.</span><span class="sxs-lookup"><span data-stu-id="4dfb4-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dfb4-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4dfb4-121">Remarks</span></span>

<span data-ttu-id="4dfb4-122">A operação externa sempre é presumida como adjointable, mas não precisa ser controlável para que a operação combinada seja controlável.</span><span class="sxs-lookup"><span data-stu-id="4dfb4-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="4dfb4-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4dfb4-123">See Also</span></span>

- [<span data-ttu-id="4dfb4-124">Microsoft. Quantum. Canon. ApplyWith</span><span class="sxs-lookup"><span data-stu-id="4dfb4-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="4dfb4-125">Microsoft. Quantum. Canon. ApplyWithA</span><span class="sxs-lookup"><span data-stu-id="4dfb4-125">Microsoft.Quantum.Canon.ApplyWithA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [<span data-ttu-id="4dfb4-126">Microsoft. Quantum. Canon. ApplyWithC</span><span class="sxs-lookup"><span data-stu-id="4dfb4-126">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)