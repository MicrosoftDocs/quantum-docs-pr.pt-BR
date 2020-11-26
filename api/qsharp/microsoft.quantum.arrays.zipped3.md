---
uid: Microsoft.Quantum.Arrays.Zipped3
title: Função Zipped3
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped3
qsharp.summary: Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: 37fda4082a46870270414649f807659fa561962b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219678"
---
# <a name="zipped3-function"></a><span data-ttu-id="2e56a-102">Função Zipped3</span><span class="sxs-lookup"><span data-stu-id="2e56a-102">Zipped3 function</span></span>

<span data-ttu-id="2e56a-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2e56a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2e56a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2e56a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2e56a-105">Dadas três matrizes, retorna uma nova matriz de 3 tuplas, de modo que cada 3 tupla contém um elemento de cada matriz original.</span><span class="sxs-lookup"><span data-stu-id="2e56a-105">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="2e56a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e56a-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="2e56a-107">Primeiro: t 1 []</span><span class="sxs-lookup"><span data-stu-id="2e56a-107">first : 'T1[]</span></span>

<span data-ttu-id="2e56a-108">Uma matriz que contém valores para o primeiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="2e56a-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="2e56a-109">Segundo: ' t 2 []</span><span class="sxs-lookup"><span data-stu-id="2e56a-109">second : 'T2[]</span></span>

<span data-ttu-id="2e56a-110">Uma matriz que contém valores para o segundo elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="2e56a-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="2e56a-111">terceiro: ' t 3 []</span><span class="sxs-lookup"><span data-stu-id="2e56a-111">third : 'T3[]</span></span>

<span data-ttu-id="2e56a-112">Uma matriz que contém valores para o terceiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="2e56a-112">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="2e56a-113">Saída: (t 1, não 2, ' t 3) []</span><span class="sxs-lookup"><span data-stu-id="2e56a-113">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="2e56a-114">Uma matriz que contém 3 tuplas do formulário `(first[idx], second[idx], third[idx])` para cada `idx` .</span><span class="sxs-lookup"><span data-stu-id="2e56a-114">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="2e56a-115">Se as três matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.</span><span class="sxs-lookup"><span data-stu-id="2e56a-115">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2e56a-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="2e56a-116">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="2e56a-117">Não 1</span><span class="sxs-lookup"><span data-stu-id="2e56a-117">'T1</span></span>

<span data-ttu-id="2e56a-118">O tipo dos primeiros elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="2e56a-118">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="2e56a-119">Não 2</span><span class="sxs-lookup"><span data-stu-id="2e56a-119">'T2</span></span>

<span data-ttu-id="2e56a-120">O tipo da segunda matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="2e56a-120">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="2e56a-121">' T 3</span><span class="sxs-lookup"><span data-stu-id="2e56a-121">'T3</span></span>

<span data-ttu-id="2e56a-122">O tipo dos elementos da terceira matriz.</span><span class="sxs-lookup"><span data-stu-id="2e56a-122">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e56a-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2e56a-123">See Also</span></span>

- [<span data-ttu-id="2e56a-124">Microsoft.Quantum.Arrays.ZipPED</span><span class="sxs-lookup"><span data-stu-id="2e56a-124">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="2e56a-125">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="2e56a-125">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)