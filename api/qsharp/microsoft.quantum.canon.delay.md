---
uid: Microsoft.Quantum.Canon.Delay
title: Operação de atraso
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: c8ba128e44a9b217ec196e39ff1df639ef276784
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840650"
---
# <a name="delay-operation"></a><span data-ttu-id="de688-102">Operação de atraso</span><span class="sxs-lookup"><span data-stu-id="de688-102">Delay operation</span></span>

<span data-ttu-id="de688-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="de688-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="de688-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="de688-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="de688-105">Aplica uma determinada operação com um atraso.</span><span class="sxs-lookup"><span data-stu-id="de688-105">Applies a given operation with a delay.</span></span>

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a><span data-ttu-id="de688-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="de688-106">Description</span></span>

<span data-ttu-id="de688-107">Dada uma operação e uma entrada para essa operação, o aplica a operação quando uma entrada adicional é fornecida.</span><span class="sxs-lookup"><span data-stu-id="de688-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="de688-108">Em particular, a expressão `Delay(op, arg, _)` é uma operação que se aplica ao `op` `arg` quando chamado.</span><span class="sxs-lookup"><span data-stu-id="de688-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="de688-109">A expressão `Delay(op,arg,_)` permite atrasar a aplicação do `op` .</span><span class="sxs-lookup"><span data-stu-id="de688-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="de688-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="de688-110">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="de688-111">op: ' T' => ' U</span><span class="sxs-lookup"><span data-stu-id="de688-111">op : 'T => 'U</span></span> 

<span data-ttu-id="de688-112">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="de688-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="de688-113">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="de688-113">arg : 'T</span></span>

<span data-ttu-id="de688-114">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="de688-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="de688-115">AUX: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="de688-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="de688-116">Argumento usado para atrasar a aplicação de operação usando o aplicativo parcial.</span><span class="sxs-lookup"><span data-stu-id="de688-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--u"></a><span data-ttu-id="de688-117">Saída: ' U</span><span class="sxs-lookup"><span data-stu-id="de688-117">Output : 'U</span></span>



## <a name="type-parameters"></a><span data-ttu-id="de688-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="de688-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="de688-119">T'</span><span class="sxs-lookup"><span data-stu-id="de688-119">'T</span></span>

<span data-ttu-id="de688-120">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="de688-120">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="de688-121">' U</span><span class="sxs-lookup"><span data-stu-id="de688-121">'U</span></span>

<span data-ttu-id="de688-122">O tipo de retorno da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="de688-122">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="de688-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="de688-123">See Also</span></span>

- [<span data-ttu-id="de688-124">Microsoft. Quantum. Canon. DelayC</span><span class="sxs-lookup"><span data-stu-id="de688-124">Microsoft.Quantum.Canon.DelayC</span></span>](xref:Microsoft.Quantum.Canon.DelayC)
- [<span data-ttu-id="de688-125">Microsoft. Quantum. Canon. Delaya</span><span class="sxs-lookup"><span data-stu-id="de688-125">Microsoft.Quantum.Canon.DelayA</span></span>](xref:Microsoft.Quantum.Canon.DelayA)
- [<span data-ttu-id="de688-126">Microsoft. Quantum. Canon. DelayCA</span><span class="sxs-lookup"><span data-stu-id="de688-126">Microsoft.Quantum.Canon.DelayCA</span></span>](xref:Microsoft.Quantum.Canon.DelayCA)
- [<span data-ttu-id="de688-127">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="de688-127">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)