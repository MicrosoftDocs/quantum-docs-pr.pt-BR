---
uid: Microsoft.Quantum.Arrays.Zip4
title: Função Zip4
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip4
qsharp.summary: >-
  > [!WARNING]

  > Zip4 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.


  Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: c9dd07ddc63f1d75952d3841997eed0f78e054b9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219780"
---
# <a name="zip4-function"></a><span data-ttu-id="e8030-102">Função Zip4</span><span class="sxs-lookup"><span data-stu-id="e8030-102">Zip4 function</span></span>

<span data-ttu-id="e8030-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e8030-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e8030-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8030-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="e8030-105">Zip4 foi preterido.</span><span class="sxs-lookup"><span data-stu-id="e8030-105">Zip4 has been deprecated.</span></span> <span data-ttu-id="e8030-106">Use <xref:Microsoft.Quantum.Arrays.Zipped4> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="e8030-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.</span></span>

<span data-ttu-id="e8030-107">Dadas quatro matrizes, retorna uma nova matriz de 4 tuplas, de modo que cada 4 tupla contém um elemento de cada matriz original.</span><span class="sxs-lookup"><span data-stu-id="e8030-107">Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.</span></span>

```qsharp
function Zip4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a><span data-ttu-id="e8030-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8030-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="e8030-109">Primeiro: t 1 []</span><span class="sxs-lookup"><span data-stu-id="e8030-109">first : 'T1[]</span></span>

<span data-ttu-id="e8030-110">Uma matriz que contém valores para o primeiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="e8030-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="e8030-111">Segundo: ' t 2 []</span><span class="sxs-lookup"><span data-stu-id="e8030-111">second : 'T2[]</span></span>

<span data-ttu-id="e8030-112">Uma matriz que contém valores para o segundo elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="e8030-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="e8030-113">terceiro: ' t 3 []</span><span class="sxs-lookup"><span data-stu-id="e8030-113">third : 'T3[]</span></span>

<span data-ttu-id="e8030-114">Uma matriz que contém valores para o terceiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="e8030-114">An array containing values for the third element of each tuple.</span></span>


### <a name="fourth--t4"></a><span data-ttu-id="e8030-115">quarto: t 4 []</span><span class="sxs-lookup"><span data-stu-id="e8030-115">fourth : 'T4[]</span></span>

<span data-ttu-id="e8030-116">Uma matriz que contém valores para o quarto elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="e8030-116">An array containing values for the fourth element of each tuple.</span></span>



## <a name="output--t1t2t3t4"></a><span data-ttu-id="e8030-117">Saída: (t 1, não 2, ' T' 3, ' t 4) []</span><span class="sxs-lookup"><span data-stu-id="e8030-117">Output : ('T1,'T2,'T3,'T4)[]</span></span>

<span data-ttu-id="e8030-118">Uma matriz que contém 4 tuplas do formulário `(first[idx], second[idx], third[idx], fourth[idx])` para cada `idx` .</span><span class="sxs-lookup"><span data-stu-id="e8030-118">An array containing 4-tuples of the form `(first[idx], second[idx], third[idx], fourth[idx])` for each `idx`.</span></span> <span data-ttu-id="e8030-119">Se as quatro matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.</span><span class="sxs-lookup"><span data-stu-id="e8030-119">If the four arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e8030-120">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e8030-120">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="e8030-121">Não 1</span><span class="sxs-lookup"><span data-stu-id="e8030-121">'T1</span></span>

<span data-ttu-id="e8030-122">O tipo dos primeiros elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="e8030-122">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="e8030-123">Não 2</span><span class="sxs-lookup"><span data-stu-id="e8030-123">'T2</span></span>

<span data-ttu-id="e8030-124">O tipo da segunda matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="e8030-124">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="e8030-125">' T 3</span><span class="sxs-lookup"><span data-stu-id="e8030-125">'T3</span></span>

<span data-ttu-id="e8030-126">O tipo dos elementos da terceira matriz.</span><span class="sxs-lookup"><span data-stu-id="e8030-126">The type of the third array elements.</span></span>
### <a name="t4"></a><span data-ttu-id="e8030-127">' T 4</span><span class="sxs-lookup"><span data-stu-id="e8030-127">'T4</span></span>

<span data-ttu-id="e8030-128">O tipo dos elementos da quarta matriz.</span><span class="sxs-lookup"><span data-stu-id="e8030-128">The type of the fourth array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8030-129">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e8030-129">See Also</span></span>

- [<span data-ttu-id="e8030-130">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="e8030-130">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="e8030-131">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="e8030-131">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)