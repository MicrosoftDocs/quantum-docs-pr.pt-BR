---
uid: Microsoft.Quantum.Math.Fraction
title: Tipo de fração definido pelo usuário
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a56d28e34938729a8e4ffda5f870e0b6a25be017
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857508"
---
# <a name="fraction-user-defined-type"></a><span data-ttu-id="72094-102">Tipo de fração definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="72094-102">Fraction user defined type</span></span>

<span data-ttu-id="72094-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="72094-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="72094-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="72094-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="72094-105">Representa um número racional do formulário `p/q` .</span><span class="sxs-lookup"><span data-stu-id="72094-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="72094-106">Integer `p` é o primeiro elemento da tupla e `q` é o segundo elemento da tupla.</span><span class="sxs-lookup"><span data-stu-id="72094-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a><span data-ttu-id="72094-107">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="72094-107">Named Items</span></span>

### <a name="numerator--int"></a><span data-ttu-id="72094-108">Numerador: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="72094-108">Numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="72094-109">Numerador da fração.</span><span class="sxs-lookup"><span data-stu-id="72094-109">Numerator of the fraction.</span></span>
### <a name="denominator--int"></a><span data-ttu-id="72094-110">Denominador: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="72094-110">Denominator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="72094-111">Denominador da fração/</span><span class="sxs-lookup"><span data-stu-id="72094-111">Denominator of the fraction/</span></span>