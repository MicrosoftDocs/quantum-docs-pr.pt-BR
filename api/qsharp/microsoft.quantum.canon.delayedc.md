---
uid: Microsoft.Quantum.Canon.DelayedC
title: Função DelayedC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 7cfd77b0bb2d91c5a1c4bb5bc84e052421d733a9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694014"
---
# <a name="delayedc-function"></a><span data-ttu-id="cea32-102">Função DelayedC</span><span class="sxs-lookup"><span data-stu-id="cea32-102">DelayedC function</span></span>

<span data-ttu-id="cea32-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cea32-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cea32-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cea32-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cea32-105">Retorna uma operação que aplica a operação especificada com o argumento fornecido.</span><span class="sxs-lookup"><span data-stu-id="cea32-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="cea32-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="cea32-106">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="cea32-107">op: ' t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cea32-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="cea32-108">Uma operação a ser aplicada como resultado da aplicação do valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cea32-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="cea32-109">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="cea32-109">arg : 'T</span></span>

<span data-ttu-id="cea32-110">A entrada à qual a operação `op` é aplicada.</span><span class="sxs-lookup"><span data-stu-id="cea32-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-ctl"></a><span data-ttu-id="cea32-111">Saída: [Unit](xref:microsoft.quantum.lang-ref.unit) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) de unidade</span><span class="sxs-lookup"><span data-stu-id="cea32-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="cea32-112">Uma nova operação que se aplica `op` com a entrada `arg`</span><span class="sxs-lookup"><span data-stu-id="cea32-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cea32-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="cea32-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cea32-114">T'</span><span class="sxs-lookup"><span data-stu-id="cea32-114">'T</span></span>

<span data-ttu-id="cea32-115">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="cea32-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="cea32-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cea32-116">See Also</span></span>

- [<span data-ttu-id="cea32-117">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="cea32-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="cea32-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="cea32-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)