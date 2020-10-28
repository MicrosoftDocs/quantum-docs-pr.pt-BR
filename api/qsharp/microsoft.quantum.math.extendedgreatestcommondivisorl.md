---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: Função ExtendedGreatestCommonDivisorL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: e671405045d6d2587a8c6ccbac4ae3402f92f722
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696839"
---
# <a name="extendedgreatestcommondivisorl-function"></a><span data-ttu-id="91b0b-102">Função ExtendedGreatestCommonDivisorL</span><span class="sxs-lookup"><span data-stu-id="91b0b-102">ExtendedGreatestCommonDivisorL function</span></span>

<span data-ttu-id="91b0b-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="91b0b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="91b0b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="91b0b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="91b0b-105">Computa uma tupla $ (u, v) $ de forma que $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, em que $ \operatorname{GCD} $ é $a $ maior divisor comum de $a $ e $b $.</span><span class="sxs-lookup"><span data-stu-id="91b0b-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="91b0b-106">O GCD é sempre positivo.</span><span class="sxs-lookup"><span data-stu-id="91b0b-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="91b0b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="91b0b-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="91b0b-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="91b0b-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="91b0b-109">o primeiro número do qual o maior divisor comum estendido está sendo computado</span><span class="sxs-lookup"><span data-stu-id="91b0b-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="91b0b-110">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="91b0b-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="91b0b-111">o segundo número do qual o maior divisor comum estendido está sendo computado</span><span class="sxs-lookup"><span data-stu-id="91b0b-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigintbigint"></a><span data-ttu-id="91b0b-112">Saída: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="91b0b-112">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>

<span data-ttu-id="91b0b-113">Tupla $ (u, v) $ com a propriedade $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="91b0b-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="91b0b-114">Referências</span><span class="sxs-lookup"><span data-stu-id="91b0b-114">References</span></span>

- <span data-ttu-id="91b0b-115">Essa implementação é de acordo com https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="91b0b-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>