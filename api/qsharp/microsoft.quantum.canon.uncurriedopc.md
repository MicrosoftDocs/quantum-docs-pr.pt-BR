---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Função UncurriedOpC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: f3e5ecf3f7df0393dfbb948f064c27505f04cfcf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693871"
---
# <a name="uncurriedopc-function"></a><span data-ttu-id="58df7-102">Função UncurriedOpC</span><span class="sxs-lookup"><span data-stu-id="58df7-102">UncurriedOpC function</span></span>

<span data-ttu-id="58df7-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="58df7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="58df7-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="58df7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="58df7-105">Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.</span><span class="sxs-lookup"><span data-stu-id="58df7-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="58df7-106">O modificador `C` indica que as operações são controláveis.</span><span class="sxs-lookup"><span data-stu-id="58df7-106">The modifier `C` indicates that the operations are controllable.</span></span>

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="58df7-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="58df7-107">Input</span></span>

### <a name="curriedop--t---u--unit-ctl"></a><span data-ttu-id="58df7-108">curriedOp: t-> ' U = CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="58df7-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="58df7-109">Uma função que retorna operações.</span><span class="sxs-lookup"><span data-stu-id="58df7-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-ctl"></a><span data-ttu-id="58df7-110">Saída: (' t, ' U) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="58df7-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="58df7-111">Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="58df7-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="58df7-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="58df7-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="58df7-113">T'</span><span class="sxs-lookup"><span data-stu-id="58df7-113">'T</span></span>

<span data-ttu-id="58df7-114">O tipo do primeiro argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="58df7-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="58df7-115">' U</span><span class="sxs-lookup"><span data-stu-id="58df7-115">'U</span></span>

<span data-ttu-id="58df7-116">O tipo do segundo argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="58df7-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="58df7-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="58df7-117">See Also</span></span>

- [<span data-ttu-id="58df7-118">Microsoft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="58df7-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)