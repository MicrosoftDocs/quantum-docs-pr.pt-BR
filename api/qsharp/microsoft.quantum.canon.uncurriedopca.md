---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Função UncurriedOpCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 910d8a3006a2f217888b791e479e10f9f1a6965e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840034"
---
# <a name="uncurriedopca-function"></a><span data-ttu-id="49376-102">Função UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="49376-102">UncurriedOpCA function</span></span>

<span data-ttu-id="49376-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="49376-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="49376-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="49376-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="49376-105">Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.</span><span class="sxs-lookup"><span data-stu-id="49376-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="49376-106">O modificador `CA` indica que as operações são controláveis e adjointable.</span><span class="sxs-lookup"><span data-stu-id="49376-106">The modifier `CA` indicates that the operations are controllable and adjointable.</span></span>

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="49376-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="49376-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj--ctl"></a><span data-ttu-id="49376-108">curriedOp: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="49376-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="49376-109">Uma função que retorna operações.</span><span class="sxs-lookup"><span data-stu-id="49376-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj--ctl"></a><span data-ttu-id="49376-110">Saída: (' t, ' U) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="49376-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="49376-111">Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="49376-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="49376-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="49376-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="49376-113">T'</span><span class="sxs-lookup"><span data-stu-id="49376-113">'T</span></span>

<span data-ttu-id="49376-114">O tipo do primeiro argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="49376-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="49376-115">' U</span><span class="sxs-lookup"><span data-stu-id="49376-115">'U</span></span>

<span data-ttu-id="49376-116">O tipo do segundo argumento de uma função na forma curried.</span><span class="sxs-lookup"><span data-stu-id="49376-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="49376-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="49376-117">See Also</span></span>

- [<span data-ttu-id="49376-118">Microsoft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="49376-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)