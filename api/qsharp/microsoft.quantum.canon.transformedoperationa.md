---
uid: Microsoft.Quantum.Canon.TransformedOperationA
title: Função TransformedOperationA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 349424a102dba7354bbaa65fffdc2b5d506a3b91
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693888"
---
# <a name="transformedoperationa-function"></a><span data-ttu-id="885c8-102">Função TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="885c8-102">TransformedOperationA function</span></span>

<span data-ttu-id="885c8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="885c8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="885c8-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="885c8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="885c8-105">Dada uma função e uma operação, retorna uma nova operação cuja entrada é transformada pela função fornecida.</span><span class="sxs-lookup"><span data-stu-id="885c8-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj)) : ('U => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="885c8-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="885c8-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="885c8-107">FN: ' U-> ' t</span><span class="sxs-lookup"><span data-stu-id="885c8-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="885c8-108">Uma função que transforma a entrada fornecida em um formulário esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="885c8-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit-adj"></a><span data-ttu-id="885c8-109">op: ' t => adj de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="885c8-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="885c8-110">A operação a ser transformada.</span><span class="sxs-lookup"><span data-stu-id="885c8-110">The operation to be transformed.</span></span>



## <a name="output--u--unit-adj"></a><span data-ttu-id="885c8-111">Saída: ' U => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="885c8-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="885c8-112">Uma nova operação tbat chamadas `fn` com sua entrada e, em seguida, passa a saída resultante para `op` .</span><span class="sxs-lookup"><span data-stu-id="885c8-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="885c8-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="885c8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="885c8-114">T'</span><span class="sxs-lookup"><span data-stu-id="885c8-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="885c8-115">' U</span><span class="sxs-lookup"><span data-stu-id="885c8-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="885c8-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="885c8-116">See Also</span></span>

- [<span data-ttu-id="885c8-117">Microsoft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="885c8-117">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="885c8-118">Microsoft. Quantum. Canon. TransformedOperationC</span><span class="sxs-lookup"><span data-stu-id="885c8-118">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="885c8-119">Microsoft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="885c8-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="885c8-120">Microsoft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="885c8-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="885c8-121">Microsoft. Quantum. Canon. composto</span><span class="sxs-lookup"><span data-stu-id="885c8-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)