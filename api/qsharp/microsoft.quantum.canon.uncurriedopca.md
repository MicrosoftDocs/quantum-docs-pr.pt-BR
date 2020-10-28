---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Função UncurriedOpCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 6a0f2e1b345d0ba3ac5c779c5dc2bfffaf659a0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693870"
---
# <a name="uncurriedopca-function"></a><span data-ttu-id="bd78c-102">Função UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="bd78c-102">UncurriedOpCA function</span></span>

<span data-ttu-id="bd78c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bd78c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bd78c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bd78c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bd78c-105">Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.</span><span class="sxs-lookup"><span data-stu-id="bd78c-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="bd78c-106">O modificador `CA` indica que as operações são controláveis e adjointable.</span><span class="sxs-lookup"><span data-stu-id="bd78c-106">The modifier `CA` indicates that the operations are controllable and adjointable.</span></span>

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="bd78c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bd78c-107">Input</span></span>

### <a name="curriedop--t---u--unit-ctl--adj"></a><span data-ttu-id="bd78c-108">curriedOp: t-> ' U => da [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj</span><span class="sxs-lookup"><span data-stu-id="bd78c-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="bd78c-109">Uma função que retorna operações.</span><span class="sxs-lookup"><span data-stu-id="bd78c-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-ctl--adj"></a><span data-ttu-id="bd78c-110">Saída: (' t, ' U) => [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj</span><span class="sxs-lookup"><span data-stu-id="bd78c-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="bd78c-111">Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="bd78c-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bd78c-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="bd78c-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bd78c-113">T'</span><span class="sxs-lookup"><span data-stu-id="bd78c-113">'T</span></span>

<span data-ttu-id="bd78c-114">O tipo do primeiro argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="bd78c-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="bd78c-115">' U</span><span class="sxs-lookup"><span data-stu-id="bd78c-115">'U</span></span>

<span data-ttu-id="bd78c-116">O tipo do segundo argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="bd78c-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd78c-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bd78c-117">See Also</span></span>

- [<span data-ttu-id="bd78c-118">Microsoft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="bd78c-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)