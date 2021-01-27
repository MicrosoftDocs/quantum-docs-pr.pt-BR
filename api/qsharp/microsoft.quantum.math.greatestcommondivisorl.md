---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorL
title: Função GreatestCommonDivisorL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorL
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 0f545f7888f5a9a353cc6000a12988648ac82dd8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856369"
---
# <a name="greatestcommondivisorl-function"></a><span data-ttu-id="1040a-102">Função GreatestCommonDivisorL</span><span class="sxs-lookup"><span data-stu-id="1040a-102">GreatestCommonDivisorL function</span></span>

<span data-ttu-id="1040a-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="1040a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="1040a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1040a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1040a-105">Computa o maior divisor comum de $a $ e $b $.</span><span class="sxs-lookup"><span data-stu-id="1040a-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="1040a-106">O GCD é sempre positivo.</span><span class="sxs-lookup"><span data-stu-id="1040a-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="1040a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1040a-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="1040a-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1040a-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1040a-109">o primeiro número do qual o maior divisor comum estendido está sendo computado</span><span class="sxs-lookup"><span data-stu-id="1040a-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="1040a-110">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1040a-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1040a-111">o segundo número do qual o maior divisor comum estendido está sendo computado</span><span class="sxs-lookup"><span data-stu-id="1040a-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigint"></a><span data-ttu-id="1040a-112">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1040a-112">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1040a-113">Maior divisor comum de $a $ e $b $</span><span class="sxs-lookup"><span data-stu-id="1040a-113">Greatest common divisor of $a$ and $b$</span></span>