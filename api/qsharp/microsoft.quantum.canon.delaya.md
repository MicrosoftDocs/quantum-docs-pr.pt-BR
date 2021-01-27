---
uid: Microsoft.Quantum.Canon.DelayA
title: Operação de atraso em
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: c7385cfcdf782347feb8d95311205a9311f4c929
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840663"
---
# <a name="delaya-operation"></a><span data-ttu-id="1d166-102">Operação de atraso em</span><span class="sxs-lookup"><span data-stu-id="1d166-102">DelayA operation</span></span>

<span data-ttu-id="1d166-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1d166-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1d166-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1d166-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1d166-105">Aplica uma determinada operação com um atraso.</span><span class="sxs-lookup"><span data-stu-id="1d166-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayA<'T> (op : ('T => Unit is Adj), arg : 'T, aux : Unit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="1d166-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d166-106">Description</span></span>

<span data-ttu-id="1d166-107">Dada uma operação e uma entrada para essa operação, o aplica a operação quando uma entrada adicional é fornecida.</span><span class="sxs-lookup"><span data-stu-id="1d166-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="1d166-108">Em particular, a expressão `Delay(op, arg, _)` é uma operação que se aplica ao `op` `arg` quando chamado.</span><span class="sxs-lookup"><span data-stu-id="1d166-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="1d166-109">A expressão `Delay(op,arg,_)` permite atrasar a aplicação do `op` .</span><span class="sxs-lookup"><span data-stu-id="1d166-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="1d166-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d166-110">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="1d166-111">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="1d166-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="1d166-112">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="1d166-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="1d166-113">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="1d166-113">arg : 'T</span></span>

<span data-ttu-id="1d166-114">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="1d166-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="1d166-115">AUX: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1d166-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="1d166-116">Argumento usado para atrasar a aplicação de operação usando o aplicativo parcial.</span><span class="sxs-lookup"><span data-stu-id="1d166-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1d166-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1d166-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1d166-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="1d166-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1d166-119">T'</span><span class="sxs-lookup"><span data-stu-id="1d166-119">'T</span></span>

<span data-ttu-id="1d166-120">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="1d166-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d166-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1d166-121">See Also</span></span>

- [<span data-ttu-id="1d166-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="1d166-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="1d166-123">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="1d166-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)