---
uid: Microsoft.Quantum.Convert.BigIntAsBoolArray
title: Função BigIntAsBoolArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BigIntAsBoolArray
qsharp.summary: Converts a given big integer to an array of Booleans. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 13ba5b6dbf477dd1a02f24da5b7aca9bdb30ad2b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693644"
---
# <a name="bigintasboolarray-function"></a><span data-ttu-id="5a279-102">Função BigIntAsBoolArray</span><span class="sxs-lookup"><span data-stu-id="5a279-102">BigIntAsBoolArray function</span></span>

<span data-ttu-id="5a279-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="5a279-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="5a279-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5a279-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5a279-105">Converte um inteiro grande em uma matriz de boolianos.</span><span class="sxs-lookup"><span data-stu-id="5a279-105">Converts a given big integer to an array of Booleans.</span></span>
<span data-ttu-id="5a279-106">O elemento 0 da matriz é o bit menos significativo do inteiro grande.</span><span class="sxs-lookup"><span data-stu-id="5a279-106">The 0 element of the array is the least significant bit of the big integer.</span></span>

```qsharp
function BigIntAsBoolArray (a : BigInt) : Bool[]
```


## <a name="input"></a><span data-ttu-id="5a279-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="5a279-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="5a279-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5a279-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bool"></a><span data-ttu-id="5a279-109">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="5a279-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="5a279-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a279-110">Remarks</span></span>

<span data-ttu-id="5a279-111">Consulte o [Construtor C# BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="5a279-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>