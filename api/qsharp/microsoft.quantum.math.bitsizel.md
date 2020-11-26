---
uid: Microsoft.Quantum.Math.BitSizeL
title: Função BitSizeL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 8b3d4cceb69619ed32977337fc0fe7401db38cbd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211042"
---
# <a name="bitsizel-function"></a><span data-ttu-id="12073-102">Função BitSizeL</span><span class="sxs-lookup"><span data-stu-id="12073-102">BitSizeL function</span></span>

<span data-ttu-id="12073-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="12073-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="12073-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="12073-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="12073-105">Para um inteiro não negativo `a` , retorna o número de bits necessários para representar `a` .</span><span class="sxs-lookup"><span data-stu-id="12073-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="12073-106">Ou seja, retorna o menor $n $, que $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="12073-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a><span data-ttu-id="12073-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="12073-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="12073-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="12073-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="12073-109">O inteiro cujo tamanho de bit deve ser calculado.</span><span class="sxs-lookup"><span data-stu-id="12073-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="12073-110">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="12073-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="12073-111">O tamanho de bit de `a` .</span><span class="sxs-lookup"><span data-stu-id="12073-111">The bit-size of `a`.</span></span>