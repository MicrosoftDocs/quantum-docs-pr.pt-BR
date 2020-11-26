---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Operação ApplyIf
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: c5a1012328fa012ee02707aa59c94ac9c44b8e87
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218828"
---
# <a name="applyif-operation"></a><span data-ttu-id="eb10e-102">Operação ApplyIf</span><span class="sxs-lookup"><span data-stu-id="eb10e-102">ApplyIf operation</span></span>

<span data-ttu-id="eb10e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="eb10e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="eb10e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eb10e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eb10e-105">Aplica uma operação com condição em um bit clássico.</span><span class="sxs-lookup"><span data-stu-id="eb10e-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="eb10e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb10e-106">Description</span></span>

<span data-ttu-id="eb10e-107">Dada uma operação `op` e um valor de bit `bit` , aplica- `op` `target` se ao If `bit` is `true` .</span><span class="sxs-lookup"><span data-stu-id="eb10e-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="eb10e-108">Se `false` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="eb10e-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="eb10e-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb10e-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="eb10e-110">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="eb10e-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="eb10e-111">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="eb10e-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="eb10e-112">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="eb10e-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="eb10e-113">um booliano que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="eb10e-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="eb10e-114">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="eb10e-114">target : 'T</span></span>

<span data-ttu-id="eb10e-115">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="eb10e-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eb10e-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb10e-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="eb10e-117">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="eb10e-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="eb10e-118">T'</span><span class="sxs-lookup"><span data-stu-id="eb10e-118">'T</span></span>

<span data-ttu-id="eb10e-119">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="eb10e-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb10e-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="eb10e-120">See Also</span></span>

- [<span data-ttu-id="eb10e-121">Microsoft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="eb10e-121">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="eb10e-122">Microsoft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="eb10e-122">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="eb10e-123">Microsoft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="eb10e-123">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)