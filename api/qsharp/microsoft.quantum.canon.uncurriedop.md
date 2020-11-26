---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: Função UncurriedOp
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: cad508f166d4af805cb98cd21a0260d9babb6a4c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204633"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="b55f0-102">Função UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="b55f0-102">UncurriedOp function</span></span>

<span data-ttu-id="b55f0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b55f0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b55f0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b55f0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b55f0-105">Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.</span><span class="sxs-lookup"><span data-stu-id="b55f0-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="b55f0-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b55f0-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="b55f0-107">curriedOp: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="b55f0-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b55f0-108">Uma função que retorna operações.</span><span class="sxs-lookup"><span data-stu-id="b55f0-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="b55f0-109">Saída: (' t, ' U) = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="b55f0-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b55f0-110">Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="b55f0-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b55f0-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b55f0-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b55f0-112">T'</span><span class="sxs-lookup"><span data-stu-id="b55f0-112">'T</span></span>

<span data-ttu-id="b55f0-113">O tipo da primeira entrada para uma operação na forma curried.</span><span class="sxs-lookup"><span data-stu-id="b55f0-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="b55f0-114">' U</span><span class="sxs-lookup"><span data-stu-id="b55f0-114">'U</span></span>

<span data-ttu-id="b55f0-115">O tipo da segunda entrada para uma operação na forma curried.</span><span class="sxs-lookup"><span data-stu-id="b55f0-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="b55f0-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b55f0-116">See Also</span></span>

- [<span data-ttu-id="b55f0-117">Microsoft. Quantum. Canon. UncurriedOpC</span><span class="sxs-lookup"><span data-stu-id="b55f0-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="b55f0-118">Microsoft. Quantum. Canon. UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="b55f0-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="b55f0-119">Microsoft. Quantum. Canon. UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="b55f0-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)