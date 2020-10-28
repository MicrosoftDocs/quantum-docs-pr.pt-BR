---
uid: Microsoft.Quantum.Canon.DelayedA
title: Função atrasada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 11c11cdd75d80d6324666ef56930f7a522121826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694019"
---
# <a name="delayeda-function"></a><span data-ttu-id="dc48a-102">Função atrasada</span><span class="sxs-lookup"><span data-stu-id="dc48a-102">DelayedA function</span></span>

<span data-ttu-id="dc48a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dc48a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dc48a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dc48a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dc48a-105">Retorna uma operação que aplica a operação especificada com o argumento fornecido.</span><span class="sxs-lookup"><span data-stu-id="dc48a-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="dc48a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc48a-106">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="dc48a-107">op: ' t => adj de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dc48a-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="dc48a-108">Uma operação a ser aplicada como resultado da aplicação do valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dc48a-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="dc48a-109">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="dc48a-109">arg : 'T</span></span>

<span data-ttu-id="dc48a-110">A entrada à qual a operação `op` é aplicada.</span><span class="sxs-lookup"><span data-stu-id="dc48a-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-adj"></a><span data-ttu-id="dc48a-111">Saída: [Unit](xref:microsoft.quantum.lang-ref.unit) => adj da [unidade](xref:microsoft.quantum.lang-ref.unit) de unidade</span><span class="sxs-lookup"><span data-stu-id="dc48a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="dc48a-112">Uma nova operação que se aplica `op` com a entrada `arg`</span><span class="sxs-lookup"><span data-stu-id="dc48a-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dc48a-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="dc48a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dc48a-114">T'</span><span class="sxs-lookup"><span data-stu-id="dc48a-114">'T</span></span>

<span data-ttu-id="dc48a-115">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="dc48a-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc48a-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="dc48a-116">See Also</span></span>

- [<span data-ttu-id="dc48a-117">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="dc48a-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="dc48a-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="dc48a-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)