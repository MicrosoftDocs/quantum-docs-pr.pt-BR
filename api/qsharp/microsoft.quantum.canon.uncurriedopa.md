---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Função UncurriedOpA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: e535d017d2665ddb76e5f422e18b8656c73171c6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204616"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="cea80-102">Função UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="cea80-102">UncurriedOpA function</span></span>

<span data-ttu-id="cea80-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cea80-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cea80-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cea80-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cea80-105">Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.</span><span class="sxs-lookup"><span data-stu-id="cea80-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="cea80-106">O modificador `A` indica que as operações são adjointable.</span><span class="sxs-lookup"><span data-stu-id="cea80-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="cea80-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="cea80-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj"></a><span data-ttu-id="cea80-108">curriedOp: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="cea80-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="cea80-109">Uma função que retorna operações.</span><span class="sxs-lookup"><span data-stu-id="cea80-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj"></a><span data-ttu-id="cea80-110">Saída: (' t, ' U) = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="cea80-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="cea80-111">Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="cea80-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cea80-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="cea80-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cea80-113">T'</span><span class="sxs-lookup"><span data-stu-id="cea80-113">'T</span></span>

<span data-ttu-id="cea80-114">O tipo do primeiro argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="cea80-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="cea80-115">' U</span><span class="sxs-lookup"><span data-stu-id="cea80-115">'U</span></span>

<span data-ttu-id="cea80-116">O tipo do segundo argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="cea80-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="cea80-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cea80-117">See Also</span></span>

- [<span data-ttu-id="cea80-118">Microsoft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="cea80-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)