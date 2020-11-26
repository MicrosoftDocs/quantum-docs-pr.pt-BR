---
uid: Microsoft.Quantum.Arrays.Zip
title: Função zip
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 44db8d38d96babd16ead5ae6dde91da23bdee2c9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219848"
---
# <a name="zip-function"></a><span data-ttu-id="04441-102">Função zip</span><span class="sxs-lookup"><span data-stu-id="04441-102">Zip function</span></span>

<span data-ttu-id="04441-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="04441-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="04441-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="04441-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="04441-105">O zip foi preterido.</span><span class="sxs-lookup"><span data-stu-id="04441-105">Zip has been deprecated.</span></span> <span data-ttu-id="04441-106">Use <xref:Microsoft.Quantum.Arrays.Zipped> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="04441-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.</span></span>

<span data-ttu-id="04441-107">Dadas duas matrizes, retorna uma nova matriz de pares, de modo que cada par contém um elemento de cada matriz original.</span><span class="sxs-lookup"><span data-stu-id="04441-107">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="04441-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="04441-108">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="04441-109">esquerda: ' t []</span><span class="sxs-lookup"><span data-stu-id="04441-109">left : 'T[]</span></span>

<span data-ttu-id="04441-110">Uma matriz que contém valores para o primeiro elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="04441-110">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="04441-111">direita: ' U []</span><span class="sxs-lookup"><span data-stu-id="04441-111">right : 'U[]</span></span>

<span data-ttu-id="04441-112">Uma matriz que contém valores para o segundo elemento de cada tupla.</span><span class="sxs-lookup"><span data-stu-id="04441-112">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="04441-113">Saída: (t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="04441-113">Output : ('T,'U)[]</span></span>

<span data-ttu-id="04441-114">Uma matriz que contém pares do formulário `(left[idx], right[idx])` para cada `idx` .</span><span class="sxs-lookup"><span data-stu-id="04441-114">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="04441-115">Se as duas matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.</span><span class="sxs-lookup"><span data-stu-id="04441-115">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="04441-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="04441-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="04441-117">T'</span><span class="sxs-lookup"><span data-stu-id="04441-117">'T</span></span>

<span data-ttu-id="04441-118">O tipo dos elementos da matriz esquerda.</span><span class="sxs-lookup"><span data-stu-id="04441-118">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="04441-119">' U</span><span class="sxs-lookup"><span data-stu-id="04441-119">'U</span></span>

<span data-ttu-id="04441-120">O tipo dos elementos da matriz direita.</span><span class="sxs-lookup"><span data-stu-id="04441-120">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="04441-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="04441-121">See Also</span></span>

- [<span data-ttu-id="04441-122">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="04441-122">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)
- [<span data-ttu-id="04441-123">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="04441-123">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)
- [<span data-ttu-id="04441-124">Microsoft. Quantum. arrays. descompactado</span><span class="sxs-lookup"><span data-stu-id="04441-124">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)