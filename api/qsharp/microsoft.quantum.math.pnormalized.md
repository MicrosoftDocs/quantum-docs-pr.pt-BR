---
uid: Microsoft.Quantum.Math.PNormalized
title: Função PNormalized
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 196bdab67528aa8672a010ac3830459e27276ce9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227515"
---
# <a name="pnormalized-function"></a><span data-ttu-id="f37ea-102">Função PNormalized</span><span class="sxs-lookup"><span data-stu-id="f37ea-102">PNormalized function</span></span>

<span data-ttu-id="f37ea-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="f37ea-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="f37ea-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f37ea-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f37ea-105">Normaliza um vetor de `Double` s na `L(p)` norma.</span><span class="sxs-lookup"><span data-stu-id="f37ea-105">Normalizes a vector of `Double`s in the `L(p)` norm.</span></span>

<span data-ttu-id="f37ea-106">Ou seja, dada uma matriz $x $ do tipo `Double[]` , isso retorna uma matriz onde todos os elementos são divididos pelo $p $-norma $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="f37ea-106">That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.</span></span>

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a><span data-ttu-id="f37ea-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f37ea-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="f37ea-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f37ea-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f37ea-109">O expoente $p $ no $p $-normal.</span><span class="sxs-lookup"><span data-stu-id="f37ea-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="f37ea-110">matriz: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f37ea-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="f37ea-111">Saída: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f37ea-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f37ea-112">A matriz $x $ normalizada pelo $p $-normal $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="f37ea-112">The array $x$ normalized by the $p$-norm $\|x\|_p$.</span></span>

## <a name="see-also"></a><span data-ttu-id="f37ea-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f37ea-113">See Also</span></span>

- [<span data-ttu-id="f37ea-114">Microsoft. Quantum. Math. PNorm</span><span class="sxs-lookup"><span data-stu-id="f37ea-114">Microsoft.Quantum.Math.PNorm</span></span>](xref:Microsoft.Quantum.Math.PNorm)