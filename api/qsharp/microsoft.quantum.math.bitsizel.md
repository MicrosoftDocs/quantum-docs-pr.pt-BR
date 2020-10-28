---
uid: Microsoft.Quantum.Math.BitSizeL
title: Função BitSizeL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 97068f12050317a9aa17c95f33650ef6f406066d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696764"
---
# <a name="bitsizel-function"></a><span data-ttu-id="3ebb1-102">Função BitSizeL</span><span class="sxs-lookup"><span data-stu-id="3ebb1-102">BitSizeL function</span></span>

<span data-ttu-id="3ebb1-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="3ebb1-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="3ebb1-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3ebb1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3ebb1-105">Para um inteiro não negativo `a` , retorna o número de bits necessários para representar `a` .</span><span class="sxs-lookup"><span data-stu-id="3ebb1-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="3ebb1-106">Ou seja, retorna o menor $n $, que $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a><span data-ttu-id="3ebb1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ebb1-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="3ebb1-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="3ebb1-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="3ebb1-109">O inteiro cujo tamanho de bit deve ser calculado.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="3ebb1-110">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3ebb1-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3ebb1-111">O tamanho de bit de `a` .</span><span class="sxs-lookup"><span data-stu-id="3ebb1-111">The bit-size of `a`.</span></span>