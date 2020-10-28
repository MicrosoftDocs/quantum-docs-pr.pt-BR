---
uid: Microsoft.Quantum.Math.ModL
title: Função ModL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModL
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: 15b11a59d189aa881da9fb514cf0fe3bc9f20201
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92695082"
---
# <a name="modl-function"></a><span data-ttu-id="d4aa6-102">Função ModL</span><span class="sxs-lookup"><span data-stu-id="d4aa6-102">ModL function</span></span>

<span data-ttu-id="d4aa6-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d4aa6-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d4aa6-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d4aa6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d4aa6-105">Retorna o módulo de um número em relação a outro número.</span><span class="sxs-lookup"><span data-stu-id="d4aa6-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="d4aa6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d4aa6-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="d4aa6-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d4aa6-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d4aa6-108">A entrada $a $ cujo módulo deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="d4aa6-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="d4aa6-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d4aa6-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d4aa6-110">O número com relação ao qual o módulo de $a $ será retornado.</span><span class="sxs-lookup"><span data-stu-id="d4aa6-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="d4aa6-111">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d4aa6-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d4aa6-112">O módulo $a \bmod b $.</span><span class="sxs-lookup"><span data-stu-id="d4aa6-112">The modulus $a \bmod b$.</span></span>