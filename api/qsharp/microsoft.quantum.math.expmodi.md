---
uid: Microsoft.Quantum.Math.ExpModI
title: Função ExpModI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 197f7351ce76ebb7684ca8014cab9ab65d9c784c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228483"
---
# <a name="expmodi-function"></a><span data-ttu-id="31458-102">Função ExpModI</span><span class="sxs-lookup"><span data-stu-id="31458-102">ExpModI function</span></span>

<span data-ttu-id="31458-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="31458-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="31458-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="31458-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="31458-105">Retorna um número inteiro elevado a uma determinada potência, com relação a um determinado módulo.</span><span class="sxs-lookup"><span data-stu-id="31458-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a><span data-ttu-id="31458-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="31458-106">Description</span></span>

<span data-ttu-id="31458-107">Deixe-nos indicar expBase por $x $, Power by $p $ e módulo por $N $.</span><span class="sxs-lookup"><span data-stu-id="31458-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="31458-108">A função retorna $x ^ p \operatorname{mod} N $.</span><span class="sxs-lookup"><span data-stu-id="31458-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="31458-109">Supomos que $N $, $x $ são positivos e a energia não é negativa.</span><span class="sxs-lookup"><span data-stu-id="31458-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="31458-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="31458-110">Input</span></span>

### <a name="expbase--int"></a><span data-ttu-id="31458-111">expBase: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31458-111">expBase : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="power--int"></a><span data-ttu-id="31458-112">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31458-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="modulus--int"></a><span data-ttu-id="31458-113">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31458-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="31458-114">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31458-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="remarks"></a><span data-ttu-id="31458-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="31458-115">Remarks</span></span>

<span data-ttu-id="31458-116">Leva tempo proporcional ao número de bits em `power` , e não ao `power` próprio.</span><span class="sxs-lookup"><span data-stu-id="31458-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>