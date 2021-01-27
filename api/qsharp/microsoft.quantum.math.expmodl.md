---
uid: Microsoft.Quantum.Math.ExpModL
title: Função ExpModL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 127f2e51e19c76f4f7973bf1ac2217d4fffd72f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848365"
---
# <a name="expmodl-function"></a><span data-ttu-id="192f5-102">Função ExpModL</span><span class="sxs-lookup"><span data-stu-id="192f5-102">ExpModL function</span></span>

<span data-ttu-id="192f5-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="192f5-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="192f5-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="192f5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="192f5-105">Retorna um número inteiro elevado a uma determinada potência, com relação a um determinado módulo.</span><span class="sxs-lookup"><span data-stu-id="192f5-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a><span data-ttu-id="192f5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="192f5-106">Description</span></span>

<span data-ttu-id="192f5-107">Deixe-nos indicar expBase por $x $, Power by $p $ e módulo por $N $.</span><span class="sxs-lookup"><span data-stu-id="192f5-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="192f5-108">A função retorna $x ^ p \operatorname{mod} N $.</span><span class="sxs-lookup"><span data-stu-id="192f5-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="192f5-109">Supomos que $N $, $x $ são positivos e a energia não é negativa.</span><span class="sxs-lookup"><span data-stu-id="192f5-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="192f5-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="192f5-110">Input</span></span>

### <a name="expbase--bigint"></a><span data-ttu-id="192f5-111">expBase: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="192f5-111">expBase : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="power--bigint"></a><span data-ttu-id="192f5-112">potência: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="192f5-112">power : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="modulus--bigint"></a><span data-ttu-id="192f5-113">módulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="192f5-113">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigint"></a><span data-ttu-id="192f5-114">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="192f5-114">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="192f5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="192f5-115">Remarks</span></span>

<span data-ttu-id="192f5-116">Leva tempo proporcional ao número de bits em `power` , e não ao `power` próprio.</span><span class="sxs-lookup"><span data-stu-id="192f5-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>