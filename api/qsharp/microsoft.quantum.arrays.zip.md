---
uid: Microsoft.Quantum.Arrays.Zip
title: Função zip
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 8ed658003f749efd31b8d841cecbb0a23a471af5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850892"
---
# <a name="zip-function"></a><span data-ttu-id="ac1d0-102">Função zip</span><span class="sxs-lookup"><span data-stu-id="ac1d0-102">Zip function</span></span>

<span data-ttu-id="ac1d0-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ac1d0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ac1d0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ac1d0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="ac1d0-105">O zip foi preterido.</span><span class="sxs-lookup"><span data-stu-id="ac1d0-105">Zip has been deprecated.</span></span> <span data-ttu-id="ac1d0-106">Use <xref:Microsoft.Quantum.Arrays.Zipped> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="ac1d0-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.</span></span>

<span data-ttu-id="ac1d0-107">Dadas duas matrizes, retorna uma nova matriz de pares, de modo que cada par contém um elemento de cada matriz original.</span><span class="sxs-lookup"><span data-stu-id="ac1d0-107">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="ac1d0-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac1d0-108">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="ac1d0-109">esquerda: ' t []</span><span class="sxs-lookup"><span data-stu-id="ac1d0-109">left : 'T[]</span></span>

<span data-ttu-id="ac1d0-110">Uma matriz que contém valores para o primeiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="ac1d0-110">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="ac1d0-111">direita: ' U []</span><span class="sxs-lookup"><span data-stu-id="ac1d0-111">right : 'U[]</span></span>

<span data-ttu-id="ac1d0-112">Uma matriz que contém valores para o segundo elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="ac1d0-112">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="ac1d0-113">Saída: (t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="ac1d0-113">Output : ('T,'U)[]</span></span>

<span data-ttu-id="ac1d0-114">Uma matriz que contém pares do formulário `(left[idx], right[idx])` para cada `idx` .</span><span class="sxs-lookup"><span data-stu-id="ac1d0-114">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="ac1d0-115">Se as duas matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.</span><span class="sxs-lookup"><span data-stu-id="ac1d0-115">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ac1d0-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ac1d0-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ac1d0-117">T'</span><span class="sxs-lookup"><span data-stu-id="ac1d0-117">'T</span></span>

<span data-ttu-id="ac1d0-118">O tipo dos elementos da matriz esquerda.</span><span class="sxs-lookup"><span data-stu-id="ac1d0-118">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="ac1d0-119">' U</span><span class="sxs-lookup"><span data-stu-id="ac1d0-119">'U</span></span>

<span data-ttu-id="ac1d0-120">O tipo dos elementos da matriz direita.</span><span class="sxs-lookup"><span data-stu-id="ac1d0-120">The type of the right array elements.</span></span>

## <a name="example"></a><span data-ttu-id="ac1d0-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ac1d0-121">Example</span></span>

```qsharp
let left = [1, 3, 71];
let right = [false, true];
let pairs = Zip(left, right); // [(1, false), (3, true)]
```

## <a name="see-also"></a><span data-ttu-id="ac1d0-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ac1d0-122">See Also</span></span>

- [<span data-ttu-id="ac1d0-123">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="ac1d0-123">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)
- [<span data-ttu-id="ac1d0-124">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="ac1d0-124">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)
- [<span data-ttu-id="ac1d0-125">Microsoft. Quantum. arrays. descompactado</span><span class="sxs-lookup"><span data-stu-id="ac1d0-125">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)