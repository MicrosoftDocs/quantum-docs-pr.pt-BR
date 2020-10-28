---
uid: Microsoft.Quantum.Math.ExpModI
title: Função ExpModI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: e31273702a9850d0162f160ca412ff6d50f38b28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696789"
---
# <a name="expmodi-function"></a><span data-ttu-id="c998e-102">Função ExpModI</span><span class="sxs-lookup"><span data-stu-id="c998e-102">ExpModI function</span></span>

<span data-ttu-id="c998e-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="c998e-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="c998e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c998e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c998e-105">Retorna um número inteiro elevado a uma determinada potência, com relação a um determinado módulo.</span><span class="sxs-lookup"><span data-stu-id="c998e-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a><span data-ttu-id="c998e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c998e-106">Description</span></span>

<span data-ttu-id="c998e-107">Deixe-nos indicar expBase por $x $, Power by $p $ e módulo por $N $.</span><span class="sxs-lookup"><span data-stu-id="c998e-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="c998e-108">A função retorna $x ^ p \operatorname{mod} N $.</span><span class="sxs-lookup"><span data-stu-id="c998e-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="c998e-109">Supomos que $N $, $x $ são positivos e a energia não é negativa.</span><span class="sxs-lookup"><span data-stu-id="c998e-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="c998e-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="c998e-110">Input</span></span>

### <a name="expbase--int"></a><span data-ttu-id="c998e-111">expBase: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c998e-111">expBase : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="power--int"></a><span data-ttu-id="c998e-112">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c998e-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="modulus--int"></a><span data-ttu-id="c998e-113">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c998e-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="c998e-114">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c998e-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="remarks"></a><span data-ttu-id="c998e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c998e-115">Remarks</span></span>

<span data-ttu-id="c998e-116">Leva tempo proporcional ao número de bits em `power` , e não ao `power` próprio.</span><span class="sxs-lookup"><span data-stu-id="c998e-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>