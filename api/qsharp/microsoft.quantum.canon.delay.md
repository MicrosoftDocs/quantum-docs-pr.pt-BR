---
uid: Microsoft.Quantum.Canon.Delay
title: Operação de atraso
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 4f45527faa49f79fccff3892e928fed09f9f0bc8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216499"
---
# <a name="delay-operation"></a><span data-ttu-id="b171f-102">Operação de atraso</span><span class="sxs-lookup"><span data-stu-id="b171f-102">Delay operation</span></span>

<span data-ttu-id="b171f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b171f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b171f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b171f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b171f-105">Aplica uma determinada operação com um atraso.</span><span class="sxs-lookup"><span data-stu-id="b171f-105">Applies a given operation with a delay.</span></span>

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a><span data-ttu-id="b171f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b171f-106">Description</span></span>

<span data-ttu-id="b171f-107">Dada uma operação e uma entrada para essa operação, o aplica a operação quando uma entrada adicional é fornecida.</span><span class="sxs-lookup"><span data-stu-id="b171f-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="b171f-108">Em particular, a expressão `Delay(op, arg, _)` é uma operação que se aplica ao `op` `arg` quando chamado.</span><span class="sxs-lookup"><span data-stu-id="b171f-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="b171f-109">A expressão `Delay(op,arg,_)` permite atrasar a aplicação do `op` .</span><span class="sxs-lookup"><span data-stu-id="b171f-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="b171f-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="b171f-110">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="b171f-111">op: ' T' => ' U</span><span class="sxs-lookup"><span data-stu-id="b171f-111">op : 'T => 'U</span></span> 

<span data-ttu-id="b171f-112">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="b171f-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="b171f-113">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="b171f-113">arg : 'T</span></span>

<span data-ttu-id="b171f-114">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="b171f-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="b171f-115">AUX: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b171f-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="b171f-116">Argumento usado para atrasar a aplicação de operação usando o aplicativo parcial.</span><span class="sxs-lookup"><span data-stu-id="b171f-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--u"></a><span data-ttu-id="b171f-117">Saída: ' U</span><span class="sxs-lookup"><span data-stu-id="b171f-117">Output : 'U</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b171f-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b171f-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b171f-119">T'</span><span class="sxs-lookup"><span data-stu-id="b171f-119">'T</span></span>

<span data-ttu-id="b171f-120">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="b171f-120">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="b171f-121">' U</span><span class="sxs-lookup"><span data-stu-id="b171f-121">'U</span></span>

<span data-ttu-id="b171f-122">O tipo de retorno da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="b171f-122">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="b171f-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b171f-123">See Also</span></span>

- [<span data-ttu-id="b171f-124">Microsoft. Quantum. Canon. DelayC</span><span class="sxs-lookup"><span data-stu-id="b171f-124">Microsoft.Quantum.Canon.DelayC</span></span>](xref:Microsoft.Quantum.Canon.DelayC)
- [<span data-ttu-id="b171f-125">Microsoft. Quantum. Canon. Delaya</span><span class="sxs-lookup"><span data-stu-id="b171f-125">Microsoft.Quantum.Canon.DelayA</span></span>](xref:Microsoft.Quantum.Canon.DelayA)
- [<span data-ttu-id="b171f-126">Microsoft. Quantum. Canon. DelayCA</span><span class="sxs-lookup"><span data-stu-id="b171f-126">Microsoft.Quantum.Canon.DelayCA</span></span>](xref:Microsoft.Quantum.Canon.DelayCA)
- [<span data-ttu-id="b171f-127">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="b171f-127">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)