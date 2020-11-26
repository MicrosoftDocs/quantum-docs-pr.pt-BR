---
uid: Microsoft.Quantum.Canon.DelayCA
title: Operação DelayCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayCA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: a32a4f4a3f5d0f253a4c4eaf28c67db8da978b0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207081"
---
# <a name="delayca-operation"></a><span data-ttu-id="1098c-102">Operação DelayCA</span><span class="sxs-lookup"><span data-stu-id="1098c-102">DelayCA operation</span></span>

<span data-ttu-id="1098c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1098c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1098c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1098c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1098c-105">Aplica uma determinada operação com um atraso.</span><span class="sxs-lookup"><span data-stu-id="1098c-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="1098c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1098c-106">Description</span></span>

<span data-ttu-id="1098c-107">Dada uma operação e uma entrada para essa operação, o aplica a operação quando uma entrada adicional é fornecida.</span><span class="sxs-lookup"><span data-stu-id="1098c-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="1098c-108">Em particular, a expressão `Delay(op, arg, _)` é uma operação que se aplica ao `op` `arg` quando chamado.</span><span class="sxs-lookup"><span data-stu-id="1098c-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="1098c-109">A expressão `Delay(op,arg,_)` permite atrasar a aplicação do `op` .</span><span class="sxs-lookup"><span data-stu-id="1098c-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="1098c-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="1098c-110">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="1098c-111">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="1098c-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1098c-112">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="1098c-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="1098c-113">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="1098c-113">arg : 'T</span></span>

<span data-ttu-id="1098c-114">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="1098c-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="1098c-115">AUX: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1098c-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="1098c-116">Argumento usado para atrasar a aplicação de operação usando o aplicativo parcial.</span><span class="sxs-lookup"><span data-stu-id="1098c-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1098c-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1098c-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1098c-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="1098c-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1098c-119">T'</span><span class="sxs-lookup"><span data-stu-id="1098c-119">'T</span></span>

<span data-ttu-id="1098c-120">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="1098c-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="1098c-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1098c-121">See Also</span></span>

- [<span data-ttu-id="1098c-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="1098c-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="1098c-123">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="1098c-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)