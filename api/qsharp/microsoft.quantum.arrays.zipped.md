---
uid: Microsoft.Quantum.Arrays.Zipped
title: Função compactada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 67170fa005675f0e5d788c9c3b350fb9a961a597
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694383"
---
# <a name="zipped-function"></a><span data-ttu-id="ca547-102">Função compactada</span><span class="sxs-lookup"><span data-stu-id="ca547-102">Zipped function</span></span>

<span data-ttu-id="ca547-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ca547-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ca547-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ca547-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ca547-105">Dadas duas matrizes, retorna uma nova matriz de pares, de modo que cada par contém um elemento de cada matriz original.</span><span class="sxs-lookup"><span data-stu-id="ca547-105">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="ca547-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ca547-106">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="ca547-107">esquerda: ' t []</span><span class="sxs-lookup"><span data-stu-id="ca547-107">left : 'T[]</span></span>

<span data-ttu-id="ca547-108">Uma matriz que contém valores para o primeiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="ca547-108">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="ca547-109">direita: ' U []</span><span class="sxs-lookup"><span data-stu-id="ca547-109">right : 'U[]</span></span>

<span data-ttu-id="ca547-110">Uma matriz que contém valores para o segundo elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="ca547-110">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="ca547-111">Saída: (t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="ca547-111">Output : ('T,'U)[]</span></span>

<span data-ttu-id="ca547-112">Uma matriz que contém pares do formulário `(left[idx], right[idx])` para cada `idx` .</span><span class="sxs-lookup"><span data-stu-id="ca547-112">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="ca547-113">Se as duas matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.</span><span class="sxs-lookup"><span data-stu-id="ca547-113">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ca547-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ca547-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ca547-115">T'</span><span class="sxs-lookup"><span data-stu-id="ca547-115">'T</span></span>

<span data-ttu-id="ca547-116">O tipo dos elementos da matriz esquerda.</span><span class="sxs-lookup"><span data-stu-id="ca547-116">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="ca547-117">' U</span><span class="sxs-lookup"><span data-stu-id="ca547-117">'U</span></span>

<span data-ttu-id="ca547-118">O tipo dos elementos da matriz direita.</span><span class="sxs-lookup"><span data-stu-id="ca547-118">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca547-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ca547-119">See Also</span></span>

- [<span data-ttu-id="ca547-120">Microsoft.Quantum.Arrays.Zipped3</span><span class="sxs-lookup"><span data-stu-id="ca547-120">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)
- [<span data-ttu-id="ca547-121">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="ca547-121">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)
- [<span data-ttu-id="ca547-122">Microsoft. Quantum. arrays. descompactado</span><span class="sxs-lookup"><span data-stu-id="ca547-122">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)