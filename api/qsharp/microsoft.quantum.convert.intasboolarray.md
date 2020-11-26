---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Função IntAsBoolArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: f89cb3d7ca29d7deaaf49573b2670534166caded
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224336"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="9e1bb-102">Função IntAsBoolArray</span><span class="sxs-lookup"><span data-stu-id="9e1bb-102">IntAsBoolArray function</span></span>

<span data-ttu-id="9e1bb-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="9e1bb-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="9e1bb-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9e1bb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9e1bb-105">Produz uma representação binária de um inteiro positivo, usando a representação little-endian para a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="9e1bb-105">Produces a binary representation of a positive integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="9e1bb-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="9e1bb-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="9e1bb-107">número: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9e1bb-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9e1bb-108">Um inteiro positivo a ser convertido em uma matriz de valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="9e1bb-108">A positive integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="9e1bb-109">bits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9e1bb-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9e1bb-110">O número de bits na representação binária de `number` .</span><span class="sxs-lookup"><span data-stu-id="9e1bb-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9e1bb-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="9e1bb-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="9e1bb-112">Uma matriz de valores Boolianos que representa `number` .</span><span class="sxs-lookup"><span data-stu-id="9e1bb-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e1bb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e1bb-113">Remarks</span></span>

<span data-ttu-id="9e1bb-114">A entrada `bits` deve estar entre 0 e 63.</span><span class="sxs-lookup"><span data-stu-id="9e1bb-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="9e1bb-115">A entrada `number` deve estar entre 0 e $2 ^ {\texttt{bits}}-$1.</span><span class="sxs-lookup"><span data-stu-id="9e1bb-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>