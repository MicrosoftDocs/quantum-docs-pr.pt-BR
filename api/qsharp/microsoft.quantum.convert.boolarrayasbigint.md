---
uid: Microsoft.Quantum.Convert.BoolArrayAsBigInt
title: Função BoolArrayAsBigInt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsBigInt
qsharp.summary: Converts a given array of Booleans to an equivalent big integer. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 5a85fd9f81cec0f2de7e7807622aab9604a4db7c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214306"
---
# <a name="boolarrayasbigint-function"></a><span data-ttu-id="d3b4f-102">Função BoolArrayAsBigInt</span><span class="sxs-lookup"><span data-stu-id="d3b4f-102">BoolArrayAsBigInt function</span></span>

<span data-ttu-id="d3b4f-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="d3b4f-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="d3b4f-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d3b4f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d3b4f-105">Converte uma determinada matriz de boolianos em um inteiro grande equivalente.</span><span class="sxs-lookup"><span data-stu-id="d3b4f-105">Converts a given array of Booleans to an equivalent big integer.</span></span>
<span data-ttu-id="d3b4f-106">O elemento 0 da matriz é o bit menos significativo do inteiro grande.</span><span class="sxs-lookup"><span data-stu-id="d3b4f-106">The 0 element of the array is the least significant bit of the big integer.</span></span>

```qsharp
function BoolArrayAsBigInt (a : Bool[]) : BigInt
```


## <a name="input"></a><span data-ttu-id="d3b4f-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3b4f-107">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="d3b4f-108">a: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="d3b4f-108">a : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>





## <a name="output--bigint"></a><span data-ttu-id="d3b4f-109">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d3b4f-109">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="d3b4f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3b4f-110">Remarks</span></span>

<span data-ttu-id="d3b4f-111">Consulte o [Construtor C# BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="d3b4f-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>