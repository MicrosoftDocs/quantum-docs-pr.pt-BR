---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Função UncurriedOpA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: feb5da771ee6cb6a750fa76f9ffd8f5a3e0b5734
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840061"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="f4df3-102">Função UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="f4df3-102">UncurriedOpA function</span></span>

<span data-ttu-id="f4df3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f4df3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f4df3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f4df3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f4df3-105">Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.</span><span class="sxs-lookup"><span data-stu-id="f4df3-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="f4df3-106">O modificador `A` indica que as operações são adjointable.</span><span class="sxs-lookup"><span data-stu-id="f4df3-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="f4df3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4df3-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj"></a><span data-ttu-id="f4df3-108">curriedOp: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="f4df3-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="f4df3-109">Uma função que retorna operações.</span><span class="sxs-lookup"><span data-stu-id="f4df3-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj"></a><span data-ttu-id="f4df3-110">Saída: (' t, ' U) = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="f4df3-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="f4df3-111">Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="f4df3-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f4df3-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f4df3-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f4df3-113">T'</span><span class="sxs-lookup"><span data-stu-id="f4df3-113">'T</span></span>

<span data-ttu-id="f4df3-114">O tipo do primeiro argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="f4df3-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="f4df3-115">' U</span><span class="sxs-lookup"><span data-stu-id="f4df3-115">'U</span></span>

<span data-ttu-id="f4df3-116">O tipo do segundo argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="f4df3-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4df3-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f4df3-117">See Also</span></span>

- [<span data-ttu-id="f4df3-118">Microsoft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="f4df3-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)