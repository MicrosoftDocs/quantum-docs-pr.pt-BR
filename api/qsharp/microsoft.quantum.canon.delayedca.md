---
uid: Microsoft.Quantum.Canon.DelayedCA
title: Função DelayedCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 8ee55e2ca7ec2cff9618b5dc66e19d88779d39ce
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694015"
---
# <a name="delayedca-function"></a><span data-ttu-id="c83d3-102">Função DelayedCA</span><span class="sxs-lookup"><span data-stu-id="c83d3-102">DelayedCA function</span></span>

<span data-ttu-id="c83d3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c83d3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c83d3-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c83d3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c83d3-105">Retorna uma operação que aplica a operação especificada com o argumento fornecido.</span><span class="sxs-lookup"><span data-stu-id="c83d3-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="c83d3-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c83d3-106">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="c83d3-107">op: ' t => da [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj</span><span class="sxs-lookup"><span data-stu-id="c83d3-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="c83d3-108">Uma operação a ser aplicada como resultado da aplicação do valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c83d3-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="c83d3-109">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="c83d3-109">arg : 'T</span></span>

<span data-ttu-id="c83d3-110">A entrada à qual a operação `op` é aplicada.</span><span class="sxs-lookup"><span data-stu-id="c83d3-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-ctl--adj"></a><span data-ttu-id="c83d3-111">Saída: unidade de unidades de [unidade](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + adj</span><span class="sxs-lookup"><span data-stu-id="c83d3-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="c83d3-112">Uma nova operação que se aplica `op` com a entrada `arg`</span><span class="sxs-lookup"><span data-stu-id="c83d3-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c83d3-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="c83d3-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c83d3-114">T'</span><span class="sxs-lookup"><span data-stu-id="c83d3-114">'T</span></span>

<span data-ttu-id="c83d3-115">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="c83d3-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="c83d3-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c83d3-116">See Also</span></span>

- [<span data-ttu-id="c83d3-117">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="c83d3-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="c83d3-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="c83d3-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)