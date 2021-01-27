---
uid: Microsoft.Quantum.Canon.DelayedCA
title: Função DelayedCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: c44e3448c471f2a20f995d4546ee54f3affb726e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840544"
---
# <a name="delayedca-function"></a><span data-ttu-id="027d8-102">Função DelayedCA</span><span class="sxs-lookup"><span data-stu-id="027d8-102">DelayedCA function</span></span>

<span data-ttu-id="027d8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="027d8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="027d8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="027d8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="027d8-105">Retorna uma operação que aplica a operação especificada com o argumento fornecido.</span><span class="sxs-lookup"><span data-stu-id="027d8-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="027d8-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="027d8-106">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="027d8-107">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="027d8-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="027d8-108">Uma operação a ser aplicada como resultado da aplicação do valor de retorno</span><span class="sxs-lookup"><span data-stu-id="027d8-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="027d8-109">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="027d8-109">arg : 'T</span></span>

<span data-ttu-id="027d8-110">A entrada à qual a operação `op` é aplicada.</span><span class="sxs-lookup"><span data-stu-id="027d8-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj--ctl"></a><span data-ttu-id="027d8-111">Saída: unidade de [unidade](xref:microsoft.quantum.lang-ref.unit) => [](xref:microsoft.quantum.lang-ref.unit) é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="027d8-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="027d8-112">Uma nova operação que se aplica `op` com a entrada `arg`</span><span class="sxs-lookup"><span data-stu-id="027d8-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="027d8-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="027d8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="027d8-114">T'</span><span class="sxs-lookup"><span data-stu-id="027d8-114">'T</span></span>

<span data-ttu-id="027d8-115">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="027d8-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="027d8-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="027d8-116">See Also</span></span>

- [<span data-ttu-id="027d8-117">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="027d8-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="027d8-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="027d8-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)