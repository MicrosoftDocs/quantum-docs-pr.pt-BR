---
uid: Microsoft.Quantum.Canon.DelayedC
title: Função DelayedC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: d8036397559b1587b806f701d89e892eea2da8f9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206997"
---
# <a name="delayedc-function"></a><span data-ttu-id="0854a-102">Função DelayedC</span><span class="sxs-lookup"><span data-stu-id="0854a-102">DelayedC function</span></span>

<span data-ttu-id="0854a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0854a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0854a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0854a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0854a-105">Retorna uma operação que aplica a operação especificada com o argumento fornecido.</span><span class="sxs-lookup"><span data-stu-id="0854a-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="0854a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0854a-106">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="0854a-107">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="0854a-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="0854a-108">Uma operação a ser aplicada como resultado da aplicação do valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0854a-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="0854a-109">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="0854a-109">arg : 'T</span></span>

<span data-ttu-id="0854a-110">A entrada à qual a operação `op` é aplicada.</span><span class="sxs-lookup"><span data-stu-id="0854a-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-ctl"></a><span data-ttu-id="0854a-111">Saída: unidade de [unidade](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) é CTL</span><span class="sxs-lookup"><span data-stu-id="0854a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="0854a-112">Uma nova operação que se aplica `op` com a entrada `arg`</span><span class="sxs-lookup"><span data-stu-id="0854a-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0854a-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="0854a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0854a-114">T'</span><span class="sxs-lookup"><span data-stu-id="0854a-114">'T</span></span>

<span data-ttu-id="0854a-115">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="0854a-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="0854a-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0854a-116">See Also</span></span>

- [<span data-ttu-id="0854a-117">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="0854a-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="0854a-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="0854a-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)