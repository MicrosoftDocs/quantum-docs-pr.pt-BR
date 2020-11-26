---
uid: Microsoft.Quantum.Math.BitSizeI
title: Função BitSizeI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 561450ef43144aa4d7820e1f15d9300018104acd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195844"
---
# <a name="bitsizei-function"></a><span data-ttu-id="75a77-102">Função BitSizeI</span><span class="sxs-lookup"><span data-stu-id="75a77-102">BitSizeI function</span></span>

<span data-ttu-id="75a77-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="75a77-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="75a77-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="75a77-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="75a77-105">Para um inteiro não negativo `a` , retorna o número de bits necessários para representar `a` .</span><span class="sxs-lookup"><span data-stu-id="75a77-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="75a77-106">Ou seja, retorna o menor $n $, que $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="75a77-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="75a77-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="75a77-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="75a77-108">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="75a77-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="75a77-109">O inteiro cujo tamanho de bit deve ser calculado.</span><span class="sxs-lookup"><span data-stu-id="75a77-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="75a77-110">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="75a77-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="75a77-111">O tamanho de bit de `a` .</span><span class="sxs-lookup"><span data-stu-id="75a77-111">The bit-size of `a`.</span></span>