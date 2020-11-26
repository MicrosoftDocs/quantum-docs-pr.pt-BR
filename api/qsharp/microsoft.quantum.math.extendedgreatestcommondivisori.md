---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorI
title: Função ExtendedGreatestCommonDivisorI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorI
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 365e91e84add0d57d5a3cf203bbf23d96979b251
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195516"
---
# <a name="extendedgreatestcommondivisori-function"></a><span data-ttu-id="e835a-102">Função ExtendedGreatestCommonDivisorI</span><span class="sxs-lookup"><span data-stu-id="e835a-102">ExtendedGreatestCommonDivisorI function</span></span>

<span data-ttu-id="e835a-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="e835a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="e835a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e835a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e835a-105">Computa uma tupla $ (u, v) $ de forma que $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, em que $ \operatorname{GCD} $ é $a $ maior divisor comum de $a $ e $b $.</span><span class="sxs-lookup"><span data-stu-id="e835a-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="e835a-106">O GCD é sempre positivo.</span><span class="sxs-lookup"><span data-stu-id="e835a-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorI (a : Int, b : Int) : (Int, Int)
```


## <a name="input"></a><span data-ttu-id="e835a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e835a-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="e835a-108">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e835a-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e835a-109">o primeiro número do qual o maior divisor comum estendido está sendo computado</span><span class="sxs-lookup"><span data-stu-id="e835a-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--int"></a><span data-ttu-id="e835a-110">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e835a-110">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e835a-111">o segundo número do qual o maior divisor comum estendido está sendo computado</span><span class="sxs-lookup"><span data-stu-id="e835a-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--intint"></a><span data-ttu-id="e835a-112">Saída: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="e835a-112">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="e835a-113">Tupla $ (u, v) $ com a propriedade $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="e835a-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="e835a-114">Referências</span><span class="sxs-lookup"><span data-stu-id="e835a-114">References</span></span>

- <span data-ttu-id="e835a-115">Essa implementação é de acordo com https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="e835a-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>