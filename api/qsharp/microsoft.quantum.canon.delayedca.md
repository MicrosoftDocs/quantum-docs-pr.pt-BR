---
uid: Microsoft.Quantum.Canon.DelayedCA
title: Função DelayedCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: fe2babb87d716185286b0864745f7ff6e637f8a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206996"
---
# <a name="delayedca-function"></a><span data-ttu-id="11bff-102">Função DelayedCA</span><span class="sxs-lookup"><span data-stu-id="11bff-102">DelayedCA function</span></span>

<span data-ttu-id="11bff-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="11bff-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="11bff-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="11bff-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="11bff-105">Retorna uma operação que aplica a operação especificada com o argumento fornecido.</span><span class="sxs-lookup"><span data-stu-id="11bff-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="11bff-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="11bff-106">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="11bff-107">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="11bff-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="11bff-108">Uma operação a ser aplicada como resultado da aplicação do valor de retorno</span><span class="sxs-lookup"><span data-stu-id="11bff-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="11bff-109">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="11bff-109">arg : 'T</span></span>

<span data-ttu-id="11bff-110">A entrada à qual a operação `op` é aplicada.</span><span class="sxs-lookup"><span data-stu-id="11bff-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj--ctl"></a><span data-ttu-id="11bff-111">Saída: unidade de [unidade](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="11bff-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="11bff-112">Uma nova operação que se aplica `op` com a entrada `arg`</span><span class="sxs-lookup"><span data-stu-id="11bff-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="11bff-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="11bff-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="11bff-114">T'</span><span class="sxs-lookup"><span data-stu-id="11bff-114">'T</span></span>

<span data-ttu-id="11bff-115">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="11bff-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="11bff-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="11bff-116">See Also</span></span>

- [<span data-ttu-id="11bff-117">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="11bff-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="11bff-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="11bff-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)