---
uid: Microsoft.Quantum.Canon.TransformedOperationC
title: Função TransformedOperationC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationC
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: b6867a076b654337f6127657189a8453c9973cc2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693887"
---
# <a name="transformedoperationc-function"></a><span data-ttu-id="5b9fe-102">Função TransformedOperationC</span><span class="sxs-lookup"><span data-stu-id="5b9fe-102">TransformedOperationC function</span></span>

<span data-ttu-id="5b9fe-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5b9fe-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5b9fe-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5b9fe-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5b9fe-105">Dada uma função e uma operação, retorna uma nova operação cuja entrada é transformada pela função fornecida.</span><span class="sxs-lookup"><span data-stu-id="5b9fe-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl)) : ('U => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="5b9fe-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b9fe-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="5b9fe-107">FN: ' U-> ' t</span><span class="sxs-lookup"><span data-stu-id="5b9fe-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="5b9fe-108">Uma função que transforma a entrada fornecida em um formulário esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="5b9fe-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit-ctl"></a><span data-ttu-id="5b9fe-109">op: ' t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b9fe-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="5b9fe-110">A operação a ser transformada.</span><span class="sxs-lookup"><span data-stu-id="5b9fe-110">The operation to be transformed.</span></span>



## <a name="output--u--unit-ctl"></a><span data-ttu-id="5b9fe-111">Saída: ' U => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b9fe-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="5b9fe-112">Uma nova operação tbat chamadas `fn` com sua entrada e, em seguida, passa a saída resultante para `op` .</span><span class="sxs-lookup"><span data-stu-id="5b9fe-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5b9fe-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="5b9fe-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5b9fe-114">T'</span><span class="sxs-lookup"><span data-stu-id="5b9fe-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="5b9fe-115">' U</span><span class="sxs-lookup"><span data-stu-id="5b9fe-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="5b9fe-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5b9fe-116">See Also</span></span>

- [<span data-ttu-id="5b9fe-117">Microsoft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="5b9fe-117">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="5b9fe-118">Microsoft. Quantum. Canon. TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="5b9fe-118">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="5b9fe-119">Microsoft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="5b9fe-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="5b9fe-120">Microsoft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="5b9fe-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="5b9fe-121">Microsoft. Quantum. Canon. composto</span><span class="sxs-lookup"><span data-stu-id="5b9fe-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)