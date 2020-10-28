---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: Função IsCoprimeI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: bdfaecb61f56967e21bf85ba190638b43685214d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696788"
---
# <a name="iscoprimei-function"></a><span data-ttu-id="60dd9-102">Função IsCoprimeI</span><span class="sxs-lookup"><span data-stu-id="60dd9-102">IsCoprimeI function</span></span>

<span data-ttu-id="60dd9-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="60dd9-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="60dd9-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="60dd9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="60dd9-105">Retornará true se $a $ e $b $ forem coprimos e false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="60dd9-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="60dd9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="60dd9-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="60dd9-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="60dd9-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="60dd9-108">o primeiro número de que coprimality está sendo testado</span><span class="sxs-lookup"><span data-stu-id="60dd9-108">the first number of which co-primality is being tested</span></span>


### <a name="b--int"></a><span data-ttu-id="60dd9-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="60dd9-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="60dd9-110">o segundo número do qual coprimality está sendo testado</span><span class="sxs-lookup"><span data-stu-id="60dd9-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="60dd9-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="60dd9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="60dd9-112">True, se $a $ e $b $ forem coprimos (por exemplo, seu maior divisor comum é 1) e false caso contrário</span><span class="sxs-lookup"><span data-stu-id="60dd9-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>