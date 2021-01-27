---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: Função IsCoprimeL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: a48f056d138499607d32b38b1fa0970745732c41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851340"
---
# <a name="iscoprimel-function"></a><span data-ttu-id="6e6d6-102">Função IsCoprimeL</span><span class="sxs-lookup"><span data-stu-id="6e6d6-102">IsCoprimeL function</span></span>

<span data-ttu-id="6e6d6-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="6e6d6-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="6e6d6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6e6d6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6e6d6-105">Retornará true se $a $ e $b $ forem coprimos e false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6e6d6-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="6e6d6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e6d6-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="6e6d6-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6e6d6-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6e6d6-108">o primeiro número de que coprimality está sendo testado</span><span class="sxs-lookup"><span data-stu-id="6e6d6-108">the first number of which co-primality is being tested</span></span>


### <a name="b--bigint"></a><span data-ttu-id="6e6d6-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6e6d6-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6e6d6-110">o segundo número do qual coprimality está sendo testado</span><span class="sxs-lookup"><span data-stu-id="6e6d6-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="6e6d6-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6e6d6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6e6d6-112">True, se $a $ e $b $ forem coprimos (por exemplo, seu maior divisor comum é 1) e false caso contrário</span><span class="sxs-lookup"><span data-stu-id="6e6d6-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>