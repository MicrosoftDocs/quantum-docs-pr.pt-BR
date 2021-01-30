---
uid: Microsoft.Quantum.Arrays.ForEach
title: Operação ForEach
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: 90dd6f94408d37d2b32d82e772a482b0e69c523f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848594"
---
# <a name="foreach-operation"></a><span data-ttu-id="d5fc2-102">Operação ForEach</span><span class="sxs-lookup"><span data-stu-id="d5fc2-102">ForEach operation</span></span>

<span data-ttu-id="d5fc2-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d5fc2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d5fc2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d5fc2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d5fc2-105">Dada uma matriz e uma operação que é definida para os elementos da matriz, retorna uma nova matriz que consiste nas imagens da matriz original sob a operação.</span><span class="sxs-lookup"><span data-stu-id="d5fc2-105">Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.</span></span>

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="d5fc2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5fc2-106">Input</span></span>

### <a name="action--t--u"></a><span data-ttu-id="d5fc2-107">ação: ' t => ' U</span><span class="sxs-lookup"><span data-stu-id="d5fc2-107">action : 'T => 'U</span></span> 

<span data-ttu-id="d5fc2-108">Uma operação de `'T` para `'U` que é aplicada a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="d5fc2-108">An operation from `'T` to `'U` that is applied to each element.</span></span>


### <a name="array--t"></a><span data-ttu-id="d5fc2-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="d5fc2-109">array : 'T[]</span></span>

<span data-ttu-id="d5fc2-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="d5fc2-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="d5fc2-111">Saída: ' U []</span><span class="sxs-lookup"><span data-stu-id="d5fc2-111">Output : 'U[]</span></span>

<span data-ttu-id="d5fc2-112">Uma matriz `'U[]` de elementos que são mapeados pela `action` operação.</span><span class="sxs-lookup"><span data-stu-id="d5fc2-112">An array `'U[]` of elements that are mapped by the `action` operation.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d5fc2-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d5fc2-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d5fc2-114">T'</span><span class="sxs-lookup"><span data-stu-id="d5fc2-114">'T</span></span>

<span data-ttu-id="d5fc2-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="d5fc2-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="d5fc2-116">' U</span><span class="sxs-lookup"><span data-stu-id="d5fc2-116">'U</span></span>

<span data-ttu-id="d5fc2-117">O tipo de resultado da `action` operação.</span><span class="sxs-lookup"><span data-stu-id="d5fc2-117">The result type of the `action` operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5fc2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5fc2-118">Remarks</span></span>

<span data-ttu-id="d5fc2-119">A operação é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e uma operação, `action : 'T -> 'U` podemos mapear os elementos da matriz e produzir uma nova matriz do tipo `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="d5fc2-119">The operation is defined for generic types, i.e., whenever we have an array `'T[]` and an operation `action : 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>