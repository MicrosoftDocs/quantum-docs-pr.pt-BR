---
uid: Microsoft.Quantum.Canon.DelayA
title: Operação de atraso em
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 77c40633824ccd9250252804b08d7400936515dd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694026"
---
# <a name="delaya-operation"></a><span data-ttu-id="dde21-102">Operação de atraso em</span><span class="sxs-lookup"><span data-stu-id="dde21-102">DelayA operation</span></span>

<span data-ttu-id="dde21-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dde21-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dde21-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dde21-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dde21-105">Aplica uma determinada operação com um atraso.</span><span class="sxs-lookup"><span data-stu-id="dde21-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayA<'T> (op : ('T => Unit is Adj), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a><span data-ttu-id="dde21-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="dde21-106">Description</span></span>

<span data-ttu-id="dde21-107">Dada uma operação e uma entrada para essa operação, o aplica a operação quando uma entrada adicional é fornecida.</span><span class="sxs-lookup"><span data-stu-id="dde21-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="dde21-108">Em particular, a expressão `Delay(op, arg, _)` é uma operação que se aplica ao `op` `arg` quando chamado.</span><span class="sxs-lookup"><span data-stu-id="dde21-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="dde21-109">A expressão `Delay(op,arg,_)` permite atrasar a aplicação do `op` .</span><span class="sxs-lookup"><span data-stu-id="dde21-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="dde21-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="dde21-110">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="dde21-111">op: ' t => adj de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dde21-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="dde21-112">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="dde21-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="dde21-113">ARG: ' t</span><span class="sxs-lookup"><span data-stu-id="dde21-113">arg : 'T</span></span>

<span data-ttu-id="dde21-114">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="dde21-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="dde21-115">AUX: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dde21-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="dde21-116">Argumento usado para atrasar a aplicação de operação usando o aplicativo parcial.</span><span class="sxs-lookup"><span data-stu-id="dde21-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dde21-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dde21-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dde21-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="dde21-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dde21-119">T'</span><span class="sxs-lookup"><span data-stu-id="dde21-119">'T</span></span>

<span data-ttu-id="dde21-120">O tipo de entrada da operação a ser atrasada.</span><span class="sxs-lookup"><span data-stu-id="dde21-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="dde21-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="dde21-121">See Also</span></span>

- [<span data-ttu-id="dde21-122">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="dde21-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="dde21-123">Microsoft. Quantum. Canon. atrasado</span><span class="sxs-lookup"><span data-stu-id="dde21-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)