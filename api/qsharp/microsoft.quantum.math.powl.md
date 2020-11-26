---
uid: Microsoft.Quantum.Math.PowL
title: Função PowL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowL
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: b3207d1854f6b69cdb5b68d354000a0b6746c0c2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228314"
---
# <a name="powl-function"></a><span data-ttu-id="a89bc-102">Função PowL</span><span class="sxs-lookup"><span data-stu-id="a89bc-102">PowL function</span></span>

<span data-ttu-id="a89bc-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a89bc-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a89bc-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a89bc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a89bc-105">Retorna um número elevado a uma determinada potência.</span><span class="sxs-lookup"><span data-stu-id="a89bc-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowL (a : BigInt, power : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="a89bc-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a89bc-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="a89bc-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a89bc-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a89bc-108">O número $a $ que deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="a89bc-108">The number $a$ that is to be raised.</span></span>


### <a name="power--int"></a><span data-ttu-id="a89bc-109">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a89bc-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a89bc-110">O Power $b $ para o qual $a $ deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="a89bc-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="a89bc-111">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a89bc-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a89bc-112">O Power $a ^ b $</span><span class="sxs-lookup"><span data-stu-id="a89bc-112">The power $a^b$</span></span>