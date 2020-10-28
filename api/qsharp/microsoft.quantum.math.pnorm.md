---
uid: Microsoft.Quantum.Math.PNorm
title: Função PNorm
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: cea85715e448305486f6d8a6c10e11da56edf3ee
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694967"
---
# <a name="pnorm-function"></a><span data-ttu-id="398cc-102">Função PNorm</span><span class="sxs-lookup"><span data-stu-id="398cc-102">PNorm function</span></span>

<span data-ttu-id="398cc-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="398cc-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="398cc-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="398cc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="398cc-105">Retorna a `L(p)` norma de um vetor de `Double` s.</span><span class="sxs-lookup"><span data-stu-id="398cc-105">Returns the `L(p)` norm of a vector of `Double`s.</span></span>

<span data-ttu-id="398cc-106">Ou seja, dada uma matriz $x $ do tipo `Double[]` , isso retorna o $p $-normal $ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $.</span><span class="sxs-lookup"><span data-stu-id="398cc-106">That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.</span></span>

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a><span data-ttu-id="398cc-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="398cc-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="398cc-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="398cc-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="398cc-109">O expoente $p $ no $p $-normal.</span><span class="sxs-lookup"><span data-stu-id="398cc-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="398cc-110">matriz: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="398cc-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="398cc-111">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="398cc-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="398cc-112">A $p $-norma $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="398cc-112">The $p$-norm $\|x\|_p$.</span></span>