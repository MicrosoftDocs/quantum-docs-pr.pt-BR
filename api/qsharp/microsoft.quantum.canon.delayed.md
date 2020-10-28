---
uid: Microsoft.Quantum.Canon.Delayed
title: Função atrasada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 820a38c2b4de2e0151d55bd88fb4f69567182f6b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694020"
---
# <a name="delayed-function"></a><span data-ttu-id="c11b6-102">Função atrasada</span><span class="sxs-lookup"><span data-stu-id="c11b6-102">Delayed function</span></span>

<span data-ttu-id="c11b6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c11b6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c11b6-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c11b6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c11b6-105">Retorna uma operação que aplica a operação especificada com o argumento fornecido.</span><span class="sxs-lookup"><span data-stu-id="c11b6-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a><span data-ttu-id="c11b6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c11b6-106">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="c11b6-107">op: ' T' => ' U</span><span class="sxs-lookup"><span data-stu-id="c11b6-107">op : 'T => 'U</span></span> 

<span data-ttu-id="c11b6-108">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="c11b6-108">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="c11b6-109">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="c11b6-109">arg : 'T</span></span>

<span data-ttu-id="c11b6-110">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="c11b6-110">The input to which the operation is applied.</span></span>



## <a name="output--unit--u"></a><span data-ttu-id="c11b6-111">Saída: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U</span><span class="sxs-lookup"><span data-stu-id="c11b6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => 'U</span></span> 

<span data-ttu-id="c11b6-112">Uma nova operação que se aplica `op` com a entrada `arg`</span><span class="sxs-lookup"><span data-stu-id="c11b6-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c11b6-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="c11b6-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c11b6-114">T'</span><span class="sxs-lookup"><span data-stu-id="c11b6-114">'T</span></span>

<span data-ttu-id="c11b6-115">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="c11b6-115">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="c11b6-116">' U</span><span class="sxs-lookup"><span data-stu-id="c11b6-116">'U</span></span>

<span data-ttu-id="c11b6-117">O tipo de retorno da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="c11b6-117">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="c11b6-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c11b6-118">See Also</span></span>

- [<span data-ttu-id="c11b6-119">Microsoft. Quantum. Canon. DelayedC</span><span class="sxs-lookup"><span data-stu-id="c11b6-119">Microsoft.Quantum.Canon.DelayedC</span></span>](xref:Microsoft.Quantum.Canon.DelayedC)
- [<span data-ttu-id="c11b6-120">Microsoft. Quantum. Canon. Delaya</span><span class="sxs-lookup"><span data-stu-id="c11b6-120">Microsoft.Quantum.Canon.DelayedA</span></span>](xref:Microsoft.Quantum.Canon.DelayedA)
- [<span data-ttu-id="c11b6-121">Microsoft. Quantum. Canon. DelayedCA</span><span class="sxs-lookup"><span data-stu-id="c11b6-121">Microsoft.Quantum.Canon.DelayedCA</span></span>](xref:Microsoft.Quantum.Canon.DelayedCA)
- [<span data-ttu-id="c11b6-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="c11b6-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)