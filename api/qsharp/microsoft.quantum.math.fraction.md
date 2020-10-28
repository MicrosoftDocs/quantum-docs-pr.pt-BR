---
uid: Microsoft.Quantum.Math.Fraction
title: Tipo de fração definido pelo usuário
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 350d470c374fc8e0a3f4c4a9a68ad8566ab88727
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696831"
---
# <a name="fraction-user-defined-type"></a><span data-ttu-id="1d6e4-102">Tipo de fração definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="1d6e4-102">Fraction user defined type</span></span>

<span data-ttu-id="1d6e4-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="1d6e4-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="1d6e4-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1d6e4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1d6e4-105">Representa um número racional do formulário `p/q` .</span><span class="sxs-lookup"><span data-stu-id="1d6e4-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="1d6e4-106">Integer `p` é o primeiro elemento da tupla e `q` é o segundo elemento da tupla.</span><span class="sxs-lookup"><span data-stu-id="1d6e4-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a><span data-ttu-id="1d6e4-107">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="1d6e4-107">Named Items</span></span>

### <a name="numerator--int"></a><span data-ttu-id="1d6e4-108">Numerador: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1d6e4-108">Numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1d6e4-109">Numerador da fração.</span><span class="sxs-lookup"><span data-stu-id="1d6e4-109">Numerator of the fraction.</span></span>
### <a name="denominator--int"></a><span data-ttu-id="1d6e4-110">Denominador: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1d6e4-110">Denominator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1d6e4-111">Denominador da fração/</span><span class="sxs-lookup"><span data-stu-id="1d6e4-111">Denominator of the fraction/</span></span>