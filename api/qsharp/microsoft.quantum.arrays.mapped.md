---
uid: Microsoft.Quantum.Arrays.Mapped
title: Função mapeada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 00ea0803faf6e8edfa748af63dd6c7e217b1de41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845683"
---
# <a name="mapped-function"></a><span data-ttu-id="2e927-102">Função mapeada</span><span class="sxs-lookup"><span data-stu-id="2e927-102">Mapped function</span></span>

<span data-ttu-id="2e927-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2e927-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2e927-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2e927-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2e927-105">Dada uma matriz e uma função que é definida para os elementos da matriz, retorna uma nova matriz que consiste nas imagens da matriz original sob a função.</span><span class="sxs-lookup"><span data-stu-id="2e927-105">Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="2e927-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e927-106">Input</span></span>

### <a name="mapper--t---u"></a><span data-ttu-id="2e927-107">mapeador: t-> ' U</span><span class="sxs-lookup"><span data-stu-id="2e927-107">mapper : 'T -> 'U</span></span>

<span data-ttu-id="2e927-108">Uma função de `'T` para `'U` que é usada para mapear elementos.</span><span class="sxs-lookup"><span data-stu-id="2e927-108">A function from `'T` to `'U` that is used to map elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="2e927-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="2e927-109">array : 'T[]</span></span>

<span data-ttu-id="2e927-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="2e927-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="2e927-111">Saída: ' U []</span><span class="sxs-lookup"><span data-stu-id="2e927-111">Output : 'U[]</span></span>

<span data-ttu-id="2e927-112">Uma matriz `'U[]` de elementos que são mapeados pela `mapper` função.</span><span class="sxs-lookup"><span data-stu-id="2e927-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2e927-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="2e927-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2e927-114">T'</span><span class="sxs-lookup"><span data-stu-id="2e927-114">'T</span></span>

<span data-ttu-id="2e927-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="2e927-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="2e927-116">' U</span><span class="sxs-lookup"><span data-stu-id="2e927-116">'U</span></span>

<span data-ttu-id="2e927-117">O tipo de resultado da `mapper` função.</span><span class="sxs-lookup"><span data-stu-id="2e927-117">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e927-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e927-118">Remarks</span></span>

<span data-ttu-id="2e927-119">A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e uma função, `mapper: 'T -> 'U` podemos mapear os elementos da matriz e produzir uma nova matriz do tipo `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="2e927-119">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `mapper: 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>