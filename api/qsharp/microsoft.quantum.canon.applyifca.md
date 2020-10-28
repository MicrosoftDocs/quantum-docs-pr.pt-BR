---
uid: Microsoft.Quantum.Canon.ApplyIfCA
title: Operação ApplyIfCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfCA
qsharp.summary: Applies a unitary operation conditioned on a classical bit.
ms.openlocfilehash: 9057c79622f15a082963d94fc261664e00322feb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694303"
---
# <a name="applyifca-operation"></a><span data-ttu-id="847ff-102">Operação ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="847ff-102">ApplyIfCA operation</span></span>

<span data-ttu-id="847ff-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="847ff-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="847ff-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="847ff-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="847ff-105">Aplica uma operação unitário com condição em um bit clássico.</span><span class="sxs-lookup"><span data-stu-id="847ff-105">Applies a unitary operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfCA<'T> (op : ('T => Unit is Ctl + Adj), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="847ff-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="847ff-106">Description</span></span>

<span data-ttu-id="847ff-107">Dada uma operação `op` e um valor de bit `bit` , aplica- `op` `target` se ao If `bit` is `true` .</span><span class="sxs-lookup"><span data-stu-id="847ff-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="847ff-108">Se `false` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="847ff-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="847ff-109">O sufixo `CA` indica que a operação a ser aplicada é unitário (controlável e adjacenttable).</span><span class="sxs-lookup"><span data-stu-id="847ff-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="847ff-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="847ff-110">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="847ff-111">op: ' t => da [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj</span><span class="sxs-lookup"><span data-stu-id="847ff-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="847ff-112">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="847ff-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="847ff-113">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="847ff-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="847ff-114">um booliano que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="847ff-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="847ff-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="847ff-115">target : 'T</span></span>

<span data-ttu-id="847ff-116">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="847ff-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="847ff-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="847ff-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="847ff-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="847ff-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="847ff-119">T'</span><span class="sxs-lookup"><span data-stu-id="847ff-119">'T</span></span>

<span data-ttu-id="847ff-120">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="847ff-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="847ff-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="847ff-121">See Also</span></span>

- [<span data-ttu-id="847ff-122">Microsoft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="847ff-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="847ff-123">Microsoft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="847ff-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="847ff-124">Microsoft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="847ff-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)