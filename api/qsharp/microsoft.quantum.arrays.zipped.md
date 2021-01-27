---
uid: Microsoft.Quantum.Arrays.Zipped
title: Função compactada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 5177ab0ade5a9ad7788e60c1028befb84b0191d4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845345"
---
# <a name="zipped-function"></a><span data-ttu-id="048f1-102">Função compactada</span><span class="sxs-lookup"><span data-stu-id="048f1-102">Zipped function</span></span>

<span data-ttu-id="048f1-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="048f1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="048f1-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="048f1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="048f1-105">Dadas duas matrizes, retorna uma nova matriz de pares, de modo que cada par contém um elemento de cada matriz original.</span><span class="sxs-lookup"><span data-stu-id="048f1-105">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="048f1-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="048f1-106">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="048f1-107">esquerda: ' t []</span><span class="sxs-lookup"><span data-stu-id="048f1-107">left : 'T[]</span></span>

<span data-ttu-id="048f1-108">Uma matriz que contém valores para o primeiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="048f1-108">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="048f1-109">direita: ' U []</span><span class="sxs-lookup"><span data-stu-id="048f1-109">right : 'U[]</span></span>

<span data-ttu-id="048f1-110">Uma matriz que contém valores para o segundo elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="048f1-110">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="048f1-111">Saída: (t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="048f1-111">Output : ('T,'U)[]</span></span>

<span data-ttu-id="048f1-112">Uma matriz que contém pares do formulário `(left[idx], right[idx])` para cada `idx` .</span><span class="sxs-lookup"><span data-stu-id="048f1-112">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="048f1-113">Se as duas matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.</span><span class="sxs-lookup"><span data-stu-id="048f1-113">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="048f1-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="048f1-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="048f1-115">T'</span><span class="sxs-lookup"><span data-stu-id="048f1-115">'T</span></span>

<span data-ttu-id="048f1-116">O tipo dos elementos da matriz esquerda.</span><span class="sxs-lookup"><span data-stu-id="048f1-116">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="048f1-117">' U</span><span class="sxs-lookup"><span data-stu-id="048f1-117">'U</span></span>

<span data-ttu-id="048f1-118">O tipo dos elementos da matriz direita.</span><span class="sxs-lookup"><span data-stu-id="048f1-118">The type of the right array elements.</span></span>

## <a name="example"></a><span data-ttu-id="048f1-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="048f1-119">Example</span></span>

```qsharp
let left = [1, 3, 71];
let right = [false, true];
let pairs = Zipped(left, right); // [(1, false), (3, true)]
```

## <a name="see-also"></a><span data-ttu-id="048f1-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="048f1-120">See Also</span></span>

- [<span data-ttu-id="048f1-121">Microsoft.Quantum.Arrays.Zipped3</span><span class="sxs-lookup"><span data-stu-id="048f1-121">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)
- [<span data-ttu-id="048f1-122">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="048f1-122">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)
- [<span data-ttu-id="048f1-123">Microsoft. Quantum. arrays. descompactado</span><span class="sxs-lookup"><span data-stu-id="048f1-123">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)