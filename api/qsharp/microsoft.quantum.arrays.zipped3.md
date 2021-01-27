---
uid: Microsoft.Quantum.Arrays.Zipped3
title: Função Zipped3
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped3
qsharp.summary: Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: 6a4ffaeff8e6248a708ab9f8f9a6ff0c2e9e08d1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842186"
---
# <a name="zipped3-function"></a><span data-ttu-id="2062e-102">Função Zipped3</span><span class="sxs-lookup"><span data-stu-id="2062e-102">Zipped3 function</span></span>

<span data-ttu-id="2062e-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2062e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2062e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2062e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2062e-105">Dadas três matrizes, retorna uma nova matriz de 3 tuplas, de modo que cada 3 tupla contém um elemento de cada matriz original.</span><span class="sxs-lookup"><span data-stu-id="2062e-105">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="2062e-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2062e-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="2062e-107">Primeiro: t 1 []</span><span class="sxs-lookup"><span data-stu-id="2062e-107">first : 'T1[]</span></span>

<span data-ttu-id="2062e-108">Uma matriz que contém valores para o primeiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="2062e-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="2062e-109">Segundo: ' t 2 []</span><span class="sxs-lookup"><span data-stu-id="2062e-109">second : 'T2[]</span></span>

<span data-ttu-id="2062e-110">Uma matriz que contém valores para o segundo elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="2062e-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="2062e-111">terceiro: ' t 3 []</span><span class="sxs-lookup"><span data-stu-id="2062e-111">third : 'T3[]</span></span>

<span data-ttu-id="2062e-112">Uma matriz que contém valores para o terceiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="2062e-112">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="2062e-113">Saída: (t 1, não 2, ' t 3) []</span><span class="sxs-lookup"><span data-stu-id="2062e-113">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="2062e-114">Uma matriz que contém 3 tuplas do formulário `(first[idx], second[idx], third[idx])` para cada `idx` .</span><span class="sxs-lookup"><span data-stu-id="2062e-114">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="2062e-115">Se as três matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.</span><span class="sxs-lookup"><span data-stu-id="2062e-115">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2062e-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="2062e-116">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="2062e-117">Não 1</span><span class="sxs-lookup"><span data-stu-id="2062e-117">'T1</span></span>

<span data-ttu-id="2062e-118">O tipo dos primeiros elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="2062e-118">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="2062e-119">Não 2</span><span class="sxs-lookup"><span data-stu-id="2062e-119">'T2</span></span>

<span data-ttu-id="2062e-120">O tipo da segunda matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="2062e-120">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="2062e-121">' T 3</span><span class="sxs-lookup"><span data-stu-id="2062e-121">'T3</span></span>

<span data-ttu-id="2062e-122">O tipo dos elementos da terceira matriz.</span><span class="sxs-lookup"><span data-stu-id="2062e-122">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="2062e-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2062e-123">See Also</span></span>

- [<span data-ttu-id="2062e-124">Microsoft.Quantum.Arrays.ZipPED</span><span class="sxs-lookup"><span data-stu-id="2062e-124">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="2062e-125">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="2062e-125">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)