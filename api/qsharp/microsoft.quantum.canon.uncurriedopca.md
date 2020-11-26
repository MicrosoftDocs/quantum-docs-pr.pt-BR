---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Função UncurriedOpCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 45526c0202e417213aab3fe7819827588e794e23
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216380"
---
# <a name="uncurriedopca-function"></a><span data-ttu-id="447bb-102">Função UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="447bb-102">UncurriedOpCA function</span></span>

<span data-ttu-id="447bb-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="447bb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="447bb-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="447bb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="447bb-105">Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.</span><span class="sxs-lookup"><span data-stu-id="447bb-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="447bb-106">O modificador `CA` indica que as operações são controláveis e adjointable.</span><span class="sxs-lookup"><span data-stu-id="447bb-106">The modifier `CA` indicates that the operations are controllable and adjointable.</span></span>

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="447bb-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="447bb-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj--ctl"></a><span data-ttu-id="447bb-108">curriedOp: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="447bb-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="447bb-109">Uma função que retorna operações.</span><span class="sxs-lookup"><span data-stu-id="447bb-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj--ctl"></a><span data-ttu-id="447bb-110">Saída: (' t, ' U) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="447bb-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="447bb-111">Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="447bb-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="447bb-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="447bb-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="447bb-113">T'</span><span class="sxs-lookup"><span data-stu-id="447bb-113">'T</span></span>

<span data-ttu-id="447bb-114">O tipo do primeiro argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="447bb-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="447bb-115">' U</span><span class="sxs-lookup"><span data-stu-id="447bb-115">'U</span></span>

<span data-ttu-id="447bb-116">O tipo do segundo argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="447bb-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="447bb-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="447bb-117">See Also</span></span>

- [<span data-ttu-id="447bb-118">Microsoft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="447bb-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)