---
uid: Microsoft.Quantum.Arrays.Zip
title: Função zip
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 32fea60fc36bfdbaa2ab2f3560f291bf4ce4fa51
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694386"
---
# <a name="zip-function"></a><span data-ttu-id="7321d-102">Função zip</span><span class="sxs-lookup"><span data-stu-id="7321d-102">Zip function</span></span>

<span data-ttu-id="7321d-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7321d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7321d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7321d-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="7321d-105">O zip foi preterido.</span><span class="sxs-lookup"><span data-stu-id="7321d-105">Zip has been deprecated.</span></span> <span data-ttu-id="7321d-106">Use <xref:Microsoft.Quantum.Arrays.Zipped> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7321d-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.</span></span>

<span data-ttu-id="7321d-107">Dadas duas matrizes, retorna uma nova matriz de pares, de modo que cada par contém um elemento de cada matriz original.</span><span class="sxs-lookup"><span data-stu-id="7321d-107">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="7321d-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="7321d-108">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="7321d-109">esquerda: ' t []</span><span class="sxs-lookup"><span data-stu-id="7321d-109">left : 'T[]</span></span>

<span data-ttu-id="7321d-110">Uma matriz que contém valores para o primeiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="7321d-110">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="7321d-111">direita: ' U []</span><span class="sxs-lookup"><span data-stu-id="7321d-111">right : 'U[]</span></span>

<span data-ttu-id="7321d-112">Uma matriz que contém valores para o segundo elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="7321d-112">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="7321d-113">Saída: (t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="7321d-113">Output : ('T,'U)[]</span></span>

<span data-ttu-id="7321d-114">Uma matriz que contém pares do formulário `(left[idx], right[idx])` para cada `idx` .</span><span class="sxs-lookup"><span data-stu-id="7321d-114">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="7321d-115">Se as duas matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.</span><span class="sxs-lookup"><span data-stu-id="7321d-115">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7321d-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="7321d-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7321d-117">T'</span><span class="sxs-lookup"><span data-stu-id="7321d-117">'T</span></span>

<span data-ttu-id="7321d-118">O tipo dos elementos da matriz esquerda.</span><span class="sxs-lookup"><span data-stu-id="7321d-118">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="7321d-119">' U</span><span class="sxs-lookup"><span data-stu-id="7321d-119">'U</span></span>

<span data-ttu-id="7321d-120">O tipo dos elementos da matriz direita.</span><span class="sxs-lookup"><span data-stu-id="7321d-120">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="7321d-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7321d-121">See Also</span></span>

- [<span data-ttu-id="7321d-122">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="7321d-122">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)
- [<span data-ttu-id="7321d-123">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="7321d-123">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)
- [<span data-ttu-id="7321d-124">Microsoft. Quantum. arrays. descompactado</span><span class="sxs-lookup"><span data-stu-id="7321d-124">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)