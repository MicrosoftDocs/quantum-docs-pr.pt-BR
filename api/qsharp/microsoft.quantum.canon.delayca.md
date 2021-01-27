---
uid: Microsoft.Quantum.Canon.DelayCA
title: Operação DelayCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayCA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: a8606cde976882bba0eb23467932b9ee0ed36696
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840615"
---
# <a name="delayca-operation"></a><span data-ttu-id="925e8-102">Operação DelayCA</span><span class="sxs-lookup"><span data-stu-id="925e8-102">DelayCA operation</span></span>

<span data-ttu-id="925e8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="925e8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="925e8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="925e8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="925e8-105">Aplica uma determinada operação com um atraso.</span><span class="sxs-lookup"><span data-stu-id="925e8-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="925e8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="925e8-106">Description</span></span>

<span data-ttu-id="925e8-107">Dada uma operação e uma entrada para essa operação, o aplica a operação quando uma entrada adicional é fornecida.</span><span class="sxs-lookup"><span data-stu-id="925e8-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="925e8-108">Em particular, a expressão `Delay(op, arg, _)` é uma operação que se aplica ao `op` `arg` quando chamado.</span><span class="sxs-lookup"><span data-stu-id="925e8-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="925e8-109">A expressão `Delay(op,arg,_)` permite atrasar a aplicação do `op` .</span><span class="sxs-lookup"><span data-stu-id="925e8-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="925e8-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="925e8-110">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="925e8-111">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="925e8-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="925e8-112">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="925e8-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="925e8-113">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="925e8-113">arg : 'T</span></span>

<span data-ttu-id="925e8-114">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="925e8-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="925e8-115">AUX: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="925e8-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="925e8-116">Argumento usado para atrasar a aplicação de operação usando o aplicativo parcial.</span><span class="sxs-lookup"><span data-stu-id="925e8-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="925e8-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="925e8-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="925e8-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="925e8-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="925e8-119">T'</span><span class="sxs-lookup"><span data-stu-id="925e8-119">'T</span></span>

<span data-ttu-id="925e8-120">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="925e8-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="925e8-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="925e8-121">See Also</span></span>

- [<span data-ttu-id="925e8-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="925e8-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="925e8-123">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="925e8-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)