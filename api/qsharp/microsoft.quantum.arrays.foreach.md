---
uid: Microsoft.Quantum.Arrays.ForEach
title: Operação ForEach
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: ab6ac6eb913095f31ba166ac27f034f2e2875acf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694465"
---
# <a name="foreach-operation"></a><span data-ttu-id="06a32-102">Operação ForEach</span><span class="sxs-lookup"><span data-stu-id="06a32-102">ForEach operation</span></span>

<span data-ttu-id="06a32-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="06a32-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="06a32-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="06a32-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="06a32-105">Dada uma matriz e uma operação que é definida para os elementos da matriz, retorna uma nova matriz que consiste nas imagens da matriz original sob a operação.</span><span class="sxs-lookup"><span data-stu-id="06a32-105">Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.</span></span>

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="06a32-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="06a32-106">Input</span></span>

### <a name="action--t--u"></a><span data-ttu-id="06a32-107">ação: ' t => ' U</span><span class="sxs-lookup"><span data-stu-id="06a32-107">action : 'T => 'U</span></span> 

<span data-ttu-id="06a32-108">Uma operação de `'T` para `'U` que é aplicada a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="06a32-108">An operation from `'T` to `'U` that is applied to each element.</span></span>


### <a name="array--t"></a><span data-ttu-id="06a32-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="06a32-109">array : 'T[]</span></span>

<span data-ttu-id="06a32-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="06a32-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="06a32-111">Saída: ' U []</span><span class="sxs-lookup"><span data-stu-id="06a32-111">Output : 'U[]</span></span>

<span data-ttu-id="06a32-112">Uma matriz `'U[]` de elementos que são mapeados pela `action` operação.</span><span class="sxs-lookup"><span data-stu-id="06a32-112">An array `'U[]` of elements that are mapped by the `action` operation.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="06a32-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="06a32-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="06a32-114">T'</span><span class="sxs-lookup"><span data-stu-id="06a32-114">'T</span></span>

<span data-ttu-id="06a32-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="06a32-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="06a32-116">' U</span><span class="sxs-lookup"><span data-stu-id="06a32-116">'U</span></span>

<span data-ttu-id="06a32-117">O tipo de resultado da `action` operação.</span><span class="sxs-lookup"><span data-stu-id="06a32-117">The result type of the `action` operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a32-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="06a32-118">Remarks</span></span>

<span data-ttu-id="06a32-119">A operação é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e uma operação, `action : 'T -> 'U` podemos mapear os elementos da matriz e produzir uma nova matriz do tipo `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="06a32-119">The operation is defined for generic types, i.e., whenever we have an array `'T[]` and an operation `action : 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>