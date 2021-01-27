---
uid: Microsoft.Quantum.Canon.ConjugatedByCA
title: Função ConjugatedByCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByCA
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: 54301f991d3bda14e2d2a0a6837ee89d299f2e04
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840827"
---
# <a name="conjugatedbyca-function"></a><span data-ttu-id="3e376-102">Função ConjugatedByCA</span><span class="sxs-lookup"><span data-stu-id="3e376-102">ConjugatedByCA function</span></span>

<span data-ttu-id="3e376-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3e376-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3e376-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3e376-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3e376-105">Dadas as operações externas e internas, retorna uma nova operação que conjuga a operação interna pela operação externa.</span><span class="sxs-lookup"><span data-stu-id="3e376-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedByCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl)) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="3e376-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e376-106">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="3e376-107">outerOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="3e376-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="3e376-108">A operação $U $ que deve ser usada para conjugar $V $.</span><span class="sxs-lookup"><span data-stu-id="3e376-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="3e376-109">Observe que a operação externa $U $ precisa ser adjointable, mas não precisa ser controlável.</span><span class="sxs-lookup"><span data-stu-id="3e376-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj--ctl"></a><span data-ttu-id="3e376-110">innerOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="3e376-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3e376-111">A operação $V $ sendo conjugada.</span><span class="sxs-lookup"><span data-stu-id="3e376-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit--is-adj--ctl"></a><span data-ttu-id="3e376-112">Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="3e376-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3e376-113">Uma nova operação cuja ação é representada pelo unitário $U ^ {\dagger} V U $.</span><span class="sxs-lookup"><span data-stu-id="3e376-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3e376-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="3e376-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3e376-115">T'</span><span class="sxs-lookup"><span data-stu-id="3e376-115">'T</span></span>

<span data-ttu-id="3e376-116">O tipo de destino no qual cada uma das operações internas e externas atuam.</span><span class="sxs-lookup"><span data-stu-id="3e376-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e376-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e376-117">Remarks</span></span>

<span data-ttu-id="3e376-118">A operação externa sempre é presumida como adjointable, mas não precisa ser controlável para que a operação combinada seja controlável.</span><span class="sxs-lookup"><span data-stu-id="3e376-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e376-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3e376-119">See Also</span></span>

- [<span data-ttu-id="3e376-120">Microsoft. Quantum. Canon. ConjugatedByA</span><span class="sxs-lookup"><span data-stu-id="3e376-120">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="3e376-121">Microsoft. Quantum. Canon. ConjugatedByC</span><span class="sxs-lookup"><span data-stu-id="3e376-121">Microsoft.Quantum.Canon.ConjugatedByC</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [<span data-ttu-id="3e376-122">Microsoft. Quantum. Canon. ConjugatedByCA</span><span class="sxs-lookup"><span data-stu-id="3e376-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="3e376-123">Microsoft. Quantum. Canon. ApplyWith</span><span class="sxs-lookup"><span data-stu-id="3e376-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)