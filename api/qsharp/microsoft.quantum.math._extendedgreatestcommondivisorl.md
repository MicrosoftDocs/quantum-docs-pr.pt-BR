---
uid: Microsoft.Quantum.Math._ExtendedGreatestCommonDivisorL
title: Função _ExtendedGreatestCommonDivisorL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: _ExtendedGreatestCommonDivisorL
qsharp.summary: Internal recursive call to calculate the GCD.
ms.openlocfilehash: c259007cac08cc0efbd25244713d62e8fe130d6f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851408"
---
# <a name="_extendedgreatestcommondivisorl-function"></a><span data-ttu-id="5957b-102">Função _ExtendedGreatestCommonDivisorL</span><span class="sxs-lookup"><span data-stu-id="5957b-102">_ExtendedGreatestCommonDivisorL function</span></span>

<span data-ttu-id="5957b-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="5957b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="5957b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5957b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5957b-105">Chamada recursiva interna para calcular o GCD.</span><span class="sxs-lookup"><span data-stu-id="5957b-105">Internal recursive call to calculate the GCD.</span></span>

```qsharp
function _ExtendedGreatestCommonDivisorL (signA : Int, signB : Int, r : (BigInt, BigInt), s : (BigInt, BigInt), t : (BigInt, BigInt)) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="5957b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5957b-106">Input</span></span>

### <a name="signa--int"></a><span data-ttu-id="5957b-107">signA: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5957b-107">signA : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="signb--int"></a><span data-ttu-id="5957b-108">signB: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5957b-108">signB : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="r--bigintbigint"></a><span data-ttu-id="5957b-109">r: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="5957b-109">r : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>




### <a name="s--bigintbigint"></a><span data-ttu-id="5957b-110">s: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="5957b-110">s : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>




### <a name="t--bigintbigint"></a><span data-ttu-id="5957b-111">t: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="5957b-111">t : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>





## <a name="output--bigintbigint"></a><span data-ttu-id="5957b-112">Saída: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="5957b-112">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>

