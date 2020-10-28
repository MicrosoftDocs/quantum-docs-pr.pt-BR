---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Operação AllowAtMostNCallsCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 1a9975d2d2026749238430b247cf47738de545cd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693564"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="77800-102">Operação AllowAtMostNCallsCA</span><span class="sxs-lookup"><span data-stu-id="77800-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="77800-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="77800-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="77800-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="77800-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="77800-105">Entre uma chamada para essa operação e seu adjacente, o declara que uma determinada operação é chamada no máximo um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="77800-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="77800-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="77800-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="77800-107">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="77800-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="77800-108">O número máximo de vezes que `op` pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="77800-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput-adj--ctl"></a><span data-ttu-id="77800-109">op: ' TInput => ' TOutput adj + CTL</span><span class="sxs-lookup"><span data-stu-id="77800-109">op : 'TInput => 'TOutput Adj + Ctl</span></span>

<span data-ttu-id="77800-110">Uma operação cujas chamadas devem ser restritas.</span><span class="sxs-lookup"><span data-stu-id="77800-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="77800-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="77800-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="77800-112">Uma mensagem a ser exibida após a falha.</span><span class="sxs-lookup"><span data-stu-id="77800-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="77800-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77800-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="77800-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="77800-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="77800-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="77800-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="77800-116">'TOutput</span><span class="sxs-lookup"><span data-stu-id="77800-116">'TOutput</span></span>



## <a name="remarks"></a><span data-ttu-id="77800-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="77800-117">Remarks</span></span>

<span data-ttu-id="77800-118">Esta operação pode ser substituída por um não op em destinos que não dão suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="77800-118">This operation may be replaced by a no-op on targets which do not support it.</span></span>