---
uid: Microsoft.Quantum.Math.ExpModL
title: Função ExpModL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 73d434bd364847b4e5e06d1a9f460424e0c50850
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696841"
---
# <a name="expmodl-function"></a><span data-ttu-id="826d2-102">Função ExpModL</span><span class="sxs-lookup"><span data-stu-id="826d2-102">ExpModL function</span></span>

<span data-ttu-id="826d2-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="826d2-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="826d2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="826d2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="826d2-105">Retorna um número inteiro elevado a uma determinada potência, com relação a um determinado módulo.</span><span class="sxs-lookup"><span data-stu-id="826d2-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a><span data-ttu-id="826d2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="826d2-106">Description</span></span>

<span data-ttu-id="826d2-107">Deixe-nos indicar expBase por $x $, Power by $p $ e módulo por $N $.</span><span class="sxs-lookup"><span data-stu-id="826d2-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="826d2-108">A função retorna $x ^ p \operatorname{mod} N $.</span><span class="sxs-lookup"><span data-stu-id="826d2-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="826d2-109">Supomos que $N $, $x $ são positivos e a energia não é negativa.</span><span class="sxs-lookup"><span data-stu-id="826d2-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="826d2-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="826d2-110">Input</span></span>

### <a name="expbase--bigint"></a><span data-ttu-id="826d2-111">expBase: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="826d2-111">expBase : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="power--bigint"></a><span data-ttu-id="826d2-112">potência: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="826d2-112">power : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="modulus--bigint"></a><span data-ttu-id="826d2-113">módulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="826d2-113">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigint"></a><span data-ttu-id="826d2-114">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="826d2-114">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="826d2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="826d2-115">Remarks</span></span>

<span data-ttu-id="826d2-116">Leva tempo proporcional ao número de bits em `power` , e não ao `power` próprio.</span><span class="sxs-lookup"><span data-stu-id="826d2-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>