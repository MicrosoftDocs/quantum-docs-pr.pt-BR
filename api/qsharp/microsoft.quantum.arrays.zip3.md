---
uid: Microsoft.Quantum.Arrays.Zip3
title: Função Zip3
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip3
qsharp.summary: >-
  > [!WARNING]

  > Zip3 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.


  Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: f4b1a769614ee9434b2141b8fcb91f34cd071bdb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694385"
---
# <a name="zip3-function"></a><span data-ttu-id="cbe07-102">Função Zip3</span><span class="sxs-lookup"><span data-stu-id="cbe07-102">Zip3 function</span></span>

<span data-ttu-id="cbe07-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="cbe07-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="cbe07-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cbe07-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="cbe07-105">Zip3 foi preterido.</span><span class="sxs-lookup"><span data-stu-id="cbe07-105">Zip3 has been deprecated.</span></span> <span data-ttu-id="cbe07-106">Use <xref:Microsoft.Quantum.Arrays.Zipped3> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="cbe07-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.</span></span>

<span data-ttu-id="cbe07-107">Dadas três matrizes, retorna uma nova matriz de 3 tuplas, de modo que cada 3 tupla contém um elemento de cada matriz original.</span><span class="sxs-lookup"><span data-stu-id="cbe07-107">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zip3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="cbe07-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbe07-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="cbe07-109">Primeiro: t 1 []</span><span class="sxs-lookup"><span data-stu-id="cbe07-109">first : 'T1[]</span></span>

<span data-ttu-id="cbe07-110">Uma matriz que contém valores para o primeiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="cbe07-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="cbe07-111">Segundo: ' t 2 []</span><span class="sxs-lookup"><span data-stu-id="cbe07-111">second : 'T2[]</span></span>

<span data-ttu-id="cbe07-112">Uma matriz que contém valores para o segundo elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="cbe07-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="cbe07-113">terceiro: ' t 3 []</span><span class="sxs-lookup"><span data-stu-id="cbe07-113">third : 'T3[]</span></span>

<span data-ttu-id="cbe07-114">Uma matriz que contém valores para o terceiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="cbe07-114">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="cbe07-115">Saída: (t 1, não 2, ' t 3) []</span><span class="sxs-lookup"><span data-stu-id="cbe07-115">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="cbe07-116">Uma matriz que contém 3 tuplas do formulário `(first[idx], second[idx], third[idx])` para cada `idx` .</span><span class="sxs-lookup"><span data-stu-id="cbe07-116">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="cbe07-117">Se as três matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.</span><span class="sxs-lookup"><span data-stu-id="cbe07-117">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cbe07-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="cbe07-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="cbe07-119">Não 1</span><span class="sxs-lookup"><span data-stu-id="cbe07-119">'T1</span></span>

<span data-ttu-id="cbe07-120">O tipo dos primeiros elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="cbe07-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="cbe07-121">Não 2</span><span class="sxs-lookup"><span data-stu-id="cbe07-121">'T2</span></span>

<span data-ttu-id="cbe07-122">O tipo da segunda matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="cbe07-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="cbe07-123">' T 3</span><span class="sxs-lookup"><span data-stu-id="cbe07-123">'T3</span></span>

<span data-ttu-id="cbe07-124">O tipo dos elementos da terceira matriz.</span><span class="sxs-lookup"><span data-stu-id="cbe07-124">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbe07-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cbe07-125">See Also</span></span>

- [<span data-ttu-id="cbe07-126">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="cbe07-126">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="cbe07-127">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="cbe07-127">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)