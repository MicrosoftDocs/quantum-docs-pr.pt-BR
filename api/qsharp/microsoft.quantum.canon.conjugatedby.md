---
uid: Microsoft.Quantum.Canon.ConjugatedBy
title: Função ConjugatedBy
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedBy
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: 37fbee9a7c11991645933a372f9f12c1fd696b66
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694051"
---
# <a name="conjugatedby-function"></a><span data-ttu-id="b1122-102">Função ConjugatedBy</span><span class="sxs-lookup"><span data-stu-id="b1122-102">ConjugatedBy function</span></span>

<span data-ttu-id="b1122-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b1122-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b1122-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b1122-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b1122-105">Dadas as operações externas e internas, retorna uma nova operação que conjuga a operação interna pela operação externa.</span><span class="sxs-lookup"><span data-stu-id="b1122-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedBy<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit)) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="b1122-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1122-106">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="b1122-107">outerOperation: t => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b1122-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="b1122-108">A operação $U $ que deve ser usada para conjugar $V $.</span><span class="sxs-lookup"><span data-stu-id="b1122-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="b1122-109">Observe que a operação externa $U $ precisa ser adjointable, mas não precisa ser controlável.</span><span class="sxs-lookup"><span data-stu-id="b1122-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit"></a><span data-ttu-id="b1122-110">innerOperation: t = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="b1122-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b1122-111">A operação $V $ sendo conjugada.</span><span class="sxs-lookup"><span data-stu-id="b1122-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="b1122-112">Saída: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="b1122-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b1122-113">Uma nova operação cuja ação é representada pelo unitário $U ^ {\dagger} V U $.</span><span class="sxs-lookup"><span data-stu-id="b1122-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b1122-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b1122-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b1122-115">T'</span><span class="sxs-lookup"><span data-stu-id="b1122-115">'T</span></span>

<span data-ttu-id="b1122-116">O tipo de destino no qual cada uma das operações internas e externas atuam.</span><span class="sxs-lookup"><span data-stu-id="b1122-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1122-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1122-117">Remarks</span></span>

<span data-ttu-id="b1122-118">A operação externa sempre é presumida como adjointable, mas não precisa ser controlável para que a operação combinada seja controlável.</span><span class="sxs-lookup"><span data-stu-id="b1122-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1122-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b1122-119">See Also</span></span>

- [<span data-ttu-id="b1122-120">Microsoft. Quantum. Canon. ConjugatedByA</span><span class="sxs-lookup"><span data-stu-id="b1122-120">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="b1122-121">Microsoft. Quantum. Canon. ConjugatedByC</span><span class="sxs-lookup"><span data-stu-id="b1122-121">Microsoft.Quantum.Canon.ConjugatedByC</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [<span data-ttu-id="b1122-122">Microsoft. Quantum. Canon. ConjugatedByCA</span><span class="sxs-lookup"><span data-stu-id="b1122-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="b1122-123">Microsoft. Quantum. Canon. ApplyWith</span><span class="sxs-lookup"><span data-stu-id="b1122-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)