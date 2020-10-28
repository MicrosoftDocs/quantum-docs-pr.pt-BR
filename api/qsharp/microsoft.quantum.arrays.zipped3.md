---
uid: Microsoft.Quantum.Arrays.Zipped3
title: Função Zipped3
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped3
qsharp.summary: Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: c0535ca4d6e0de13bf809a21e69d100dcb798d1f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694380"
---
# <a name="zipped3-function"></a><span data-ttu-id="469c4-102">Função Zipped3</span><span class="sxs-lookup"><span data-stu-id="469c4-102">Zipped3 function</span></span>

<span data-ttu-id="469c4-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="469c4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="469c4-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="469c4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="469c4-105">Dadas três matrizes, retorna uma nova matriz de 3 tuplas, de modo que cada 3 tupla contém um elemento de cada matriz original.</span><span class="sxs-lookup"><span data-stu-id="469c4-105">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="469c4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="469c4-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="469c4-107">Primeiro: t 1 []</span><span class="sxs-lookup"><span data-stu-id="469c4-107">first : 'T1[]</span></span>

<span data-ttu-id="469c4-108">Uma matriz que contém valores para o primeiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="469c4-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="469c4-109">Segundo: ' t 2 []</span><span class="sxs-lookup"><span data-stu-id="469c4-109">second : 'T2[]</span></span>

<span data-ttu-id="469c4-110">Uma matriz que contém valores para o segundo elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="469c4-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="469c4-111">terceiro: ' t 3 []</span><span class="sxs-lookup"><span data-stu-id="469c4-111">third : 'T3[]</span></span>

<span data-ttu-id="469c4-112">Uma matriz que contém valores para o terceiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="469c4-112">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="469c4-113">Saída: (t 1, não 2, ' t 3) []</span><span class="sxs-lookup"><span data-stu-id="469c4-113">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="469c4-114">Uma matriz que contém 3 tuplas do formulário `(first[idx], second[idx], third[idx])` para cada `idx` .</span><span class="sxs-lookup"><span data-stu-id="469c4-114">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="469c4-115">Se as três matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.</span><span class="sxs-lookup"><span data-stu-id="469c4-115">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="469c4-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="469c4-116">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="469c4-117">Não 1</span><span class="sxs-lookup"><span data-stu-id="469c4-117">'T1</span></span>

<span data-ttu-id="469c4-118">O tipo dos primeiros elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="469c4-118">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="469c4-119">Não 2</span><span class="sxs-lookup"><span data-stu-id="469c4-119">'T2</span></span>

<span data-ttu-id="469c4-120">O tipo da segunda matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="469c4-120">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="469c4-121">' T 3</span><span class="sxs-lookup"><span data-stu-id="469c4-121">'T3</span></span>

<span data-ttu-id="469c4-122">O tipo dos elementos da terceira matriz.</span><span class="sxs-lookup"><span data-stu-id="469c4-122">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="469c4-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="469c4-123">See Also</span></span>

- [<span data-ttu-id="469c4-124">Microsoft.Quantum.Arrays.ZipPED</span><span class="sxs-lookup"><span data-stu-id="469c4-124">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="469c4-125">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="469c4-125">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)