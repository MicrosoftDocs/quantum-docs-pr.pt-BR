---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: Função UncurriedOp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: 359c0b2a9dd56445fb39fadc6580809dd9fbf628
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693875"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="c60bc-102">Função UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="c60bc-102">UncurriedOp function</span></span>

<span data-ttu-id="c60bc-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c60bc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c60bc-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c60bc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c60bc-105">Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.</span><span class="sxs-lookup"><span data-stu-id="c60bc-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="c60bc-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c60bc-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="c60bc-107">curriedOp: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="c60bc-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c60bc-108">Uma função que retorna operações.</span><span class="sxs-lookup"><span data-stu-id="c60bc-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="c60bc-109">Saída: (' t, ' U) = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="c60bc-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c60bc-110">Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="c60bc-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c60bc-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="c60bc-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c60bc-112">T'</span><span class="sxs-lookup"><span data-stu-id="c60bc-112">'T</span></span>

<span data-ttu-id="c60bc-113">O tipo da primeira entrada para uma operação na forma curried.</span><span class="sxs-lookup"><span data-stu-id="c60bc-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="c60bc-114">' U</span><span class="sxs-lookup"><span data-stu-id="c60bc-114">'U</span></span>

<span data-ttu-id="c60bc-115">O tipo da segunda entrada para uma operação na forma curried.</span><span class="sxs-lookup"><span data-stu-id="c60bc-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="c60bc-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c60bc-116">See Also</span></span>

- [<span data-ttu-id="c60bc-117">Microsoft. Quantum. Canon. UncurriedOpC</span><span class="sxs-lookup"><span data-stu-id="c60bc-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="c60bc-118">Microsoft. Quantum. Canon. UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="c60bc-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="c60bc-119">Microsoft. Quantum. Canon. UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="c60bc-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)