---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Função IntAsBoolArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 8b3d230605cc756a5da01e45e47f91c5b8e9f541
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833299"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="cbb4a-102">Função IntAsBoolArray</span><span class="sxs-lookup"><span data-stu-id="cbb4a-102">IntAsBoolArray function</span></span>

<span data-ttu-id="cbb4a-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="cbb4a-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="cbb4a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cbb4a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cbb4a-105">Produz uma representação binária de um inteiro não negativo, usando a representação little-endian para a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-105">Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="cbb4a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb4a-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="cbb4a-107">número: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cbb4a-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cbb4a-108">Um inteiro não negativo a ser convertido em uma matriz de valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-108">A non-negative integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="cbb4a-109">bits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cbb4a-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cbb4a-110">O número de bits na representação binária de `number` .</span><span class="sxs-lookup"><span data-stu-id="cbb4a-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="cbb4a-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="cbb4a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="cbb4a-112">Uma matriz de valores Boolianos que representa `number` .</span><span class="sxs-lookup"><span data-stu-id="cbb4a-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbb4a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbb4a-113">Remarks</span></span>

<span data-ttu-id="cbb4a-114">A entrada `bits` deve estar entre 0 e 63.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="cbb4a-115">A entrada `number` deve estar entre 0 e $2 ^ {\texttt{bits}}-$1.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>