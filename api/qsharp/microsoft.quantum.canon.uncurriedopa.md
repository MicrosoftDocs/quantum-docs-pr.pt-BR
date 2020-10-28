---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Função UncurriedOpA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: 21df20354ad2388891f32b1bf1c7781287904983
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693872"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="7960b-102">Função UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="7960b-102">UncurriedOpA function</span></span>

<span data-ttu-id="7960b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7960b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7960b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7960b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7960b-105">Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.</span><span class="sxs-lookup"><span data-stu-id="7960b-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="7960b-106">O modificador `A` indica que as operações são adjointable.</span><span class="sxs-lookup"><span data-stu-id="7960b-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="7960b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7960b-107">Input</span></span>

### <a name="curriedop--t---u--unit-adj"></a><span data-ttu-id="7960b-108">curriedOp: t-> ' U => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7960b-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="7960b-109">Uma função que retorna operações.</span><span class="sxs-lookup"><span data-stu-id="7960b-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-adj"></a><span data-ttu-id="7960b-110">Saída: (' t, ' U) => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7960b-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="7960b-111">Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="7960b-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7960b-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="7960b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7960b-113">T'</span><span class="sxs-lookup"><span data-stu-id="7960b-113">'T</span></span>

<span data-ttu-id="7960b-114">O tipo do primeiro argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="7960b-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="7960b-115">' U</span><span class="sxs-lookup"><span data-stu-id="7960b-115">'U</span></span>

<span data-ttu-id="7960b-116">O tipo do segundo argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="7960b-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="7960b-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7960b-117">See Also</span></span>

- [<span data-ttu-id="7960b-118">Microsoft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="7960b-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)