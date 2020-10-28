---
uid: Microsoft.Quantum.Arrays.EqualA
title: Função equala
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 24fd76aaeb66081d6d8f1eaa3056117f54b5a5e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694479"
---
# <a name="equala-function"></a><span data-ttu-id="21121-102">Função equala</span><span class="sxs-lookup"><span data-stu-id="21121-102">EqualA function</span></span>

<span data-ttu-id="21121-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="21121-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="21121-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="21121-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="21121-105">Dadas duas matrizes do mesmo tipo e um predicado que é definido para pares de elementos das matrizes, verifica se as matrizes são iguais.</span><span class="sxs-lookup"><span data-stu-id="21121-105">Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.</span></span>

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="21121-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="21121-106">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="21121-107">igual: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="21121-107">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="21121-108">Uma função de tupla `('T, 'T)` para `Bool` que é usada para verificar se dois elementos de matrizes são iguais.</span><span class="sxs-lookup"><span data-stu-id="21121-108">A function from tuple `('T, 'T)` to `Bool` that is used to check whether two elements of arrays are equal.</span></span>


### <a name="array1--t"></a><span data-ttu-id="21121-109">matriz1: ' t []</span><span class="sxs-lookup"><span data-stu-id="21121-109">array1 : 'T[]</span></span>

<span data-ttu-id="21121-110">A primeira matriz a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="21121-110">The first array to be compared.</span></span>


### <a name="array2--t"></a><span data-ttu-id="21121-111">matriz2: ' t []</span><span class="sxs-lookup"><span data-stu-id="21121-111">array2 : 'T[]</span></span>

<span data-ttu-id="21121-112">A segunda matriz a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="21121-112">The second array to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="21121-113">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="21121-113">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="21121-114">O valor `true` se e somente se `array1` e `array2` forem iguais.</span><span class="sxs-lookup"><span data-stu-id="21121-114">The value `true` if and only if `array1` and `array2` are equal.</span></span>
<span data-ttu-id="21121-115">Ou seja, se ambas as matrizes tiverem o mesmo comprimento e todos os elementos forem iguais, conforme definido pelo `equal` .</span><span class="sxs-lookup"><span data-stu-id="21121-115">That is, if both arrays have the same length, and all elements are equal as defined by `equal`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="21121-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="21121-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="21121-117">T'</span><span class="sxs-lookup"><span data-stu-id="21121-117">'T</span></span>

<span data-ttu-id="21121-118">O tipo dos elementos de cada matriz.</span><span class="sxs-lookup"><span data-stu-id="21121-118">The type of each array's elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="21121-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="21121-119">Remarks</span></span>

<span data-ttu-id="21121-120">Essa função é definida para tipos genéricos; ou seja, sempre que tivermos duas matrizes `'T[]` e uma função `equal: ('T, 'T) -> Bool` , essa função retornará um `Bool` valor que indica se as matrizes são iguais.</span><span class="sxs-lookup"><span data-stu-id="21121-120">This function is defined for generic types; i.e., whenever we have two arrays `'T[]` and a function `equal: ('T, 'T) -> Bool`, this function returns a `Bool` value that indicates whether the arrays are equal.</span></span>
<span data-ttu-id="21121-121">Para que duas matrizes sejam consideradas iguais, elas precisam ter comprimento igual e os elementos nas mesmas posições nas matrizes devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="21121-121">For two arrays to be considered equal, they have to have equal length and the elements in the same positions in the arrays have to be equal.</span></span>