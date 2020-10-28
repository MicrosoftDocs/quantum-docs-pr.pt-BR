---
uid: Microsoft.Quantum.Math.BigFraction
title: Tipo definido pelo usuário BigFraction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a8daa54947097b95040a2dfa7a4d1b90bfaff856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696767"
---
# <a name="bigfraction-user-defined-type"></a><span data-ttu-id="558e0-102">Tipo definido pelo usuário BigFraction</span><span class="sxs-lookup"><span data-stu-id="558e0-102">BigFraction user defined type</span></span>

<span data-ttu-id="558e0-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="558e0-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="558e0-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="558e0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="558e0-105">Representa um número racional do formulário `p/q` .</span><span class="sxs-lookup"><span data-stu-id="558e0-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="558e0-106">Integer `p` é o primeiro elemento da tupla e `q` é o segundo elemento da tupla.</span><span class="sxs-lookup"><span data-stu-id="558e0-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a><span data-ttu-id="558e0-107">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="558e0-107">Named Items</span></span>

### <a name="numerator--bigint"></a><span data-ttu-id="558e0-108">Numerador: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="558e0-108">Numerator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="558e0-109">Numerador da fração.</span><span class="sxs-lookup"><span data-stu-id="558e0-109">Numerator of the fraction.</span></span>
### <a name="denominator--bigint"></a><span data-ttu-id="558e0-110">Denominador: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="558e0-110">Denominator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="558e0-111">Denominador da fração/</span><span class="sxs-lookup"><span data-stu-id="558e0-111">Denominator of the fraction/</span></span>