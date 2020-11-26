---
uid: Microsoft.Quantum.Math.Fraction
title: Tipo de fração definido pelo usuário
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1838bb2b605b109742948ec0633b08ca01baea98
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210668"
---
# <a name="fraction-user-defined-type"></a><span data-ttu-id="9f663-102">Tipo de fração definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="9f663-102">Fraction user defined type</span></span>

<span data-ttu-id="9f663-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="9f663-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="9f663-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9f663-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9f663-105">Representa um número racional do formulário `p/q` .</span><span class="sxs-lookup"><span data-stu-id="9f663-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="9f663-106">Integer `p` é o primeiro elemento da tupla e `q` é o segundo elemento da tupla.</span><span class="sxs-lookup"><span data-stu-id="9f663-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a><span data-ttu-id="9f663-107">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="9f663-107">Named Items</span></span>

### <a name="numerator--int"></a><span data-ttu-id="9f663-108">Numerador: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9f663-108">Numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9f663-109">Numerador da fração.</span><span class="sxs-lookup"><span data-stu-id="9f663-109">Numerator of the fraction.</span></span>
### <a name="denominator--int"></a><span data-ttu-id="9f663-110">Denominador: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9f663-110">Denominator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9f663-111">Denominador da fração/</span><span class="sxs-lookup"><span data-stu-id="9f663-111">Denominator of the fraction/</span></span>