---
uid: Microsoft.Quantum.Arrays.Unique
title: Função Unique
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: c5d40bb82f2de640e9c78eef0c27e4766b477826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694395"
---
# <a name="unique-function"></a><span data-ttu-id="4116a-102">Função Unique</span><span class="sxs-lookup"><span data-stu-id="4116a-102">Unique function</span></span>

<span data-ttu-id="4116a-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4116a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4116a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4116a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4116a-105">Retorna uma nova matriz que não tem nenhum elemento adjacente igual.</span><span class="sxs-lookup"><span data-stu-id="4116a-105">Returns a new array that has no equal adjacent elements.</span></span>

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="4116a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4116a-106">Description</span></span>

<span data-ttu-id="4116a-107">Dada parte de uma matriz de elementos e uma função para testar a igualdade, essa função retorna uma nova matriz na qual a ordem relativa dos elementos é mantida, mas todos os elementos adjacentes que são iguais são filtrados para apenas um único elemento.</span><span class="sxs-lookup"><span data-stu-id="4116a-107">Given some array of elements and a function to test equality, this function returns a new array in which the relative order of elements is kept, but all adjacent elements which are equal are filtered to just a single element.</span></span>

## <a name="input"></a><span data-ttu-id="4116a-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="4116a-108">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="4116a-109">igual: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4116a-109">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4116a-110">Uma função que compara dois elementos, de modo que `a` é considerado igual a `b` If `equal(a, b)` is `true` .</span><span class="sxs-lookup"><span data-stu-id="4116a-110">A function that compares two elements such that `a` is considered to be equal to `b` if `equal(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="4116a-111">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="4116a-111">array : 'T[]</span></span>

<span data-ttu-id="4116a-112">A matriz a ser filtrada para elementos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="4116a-112">The array to be filtered for unique elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="4116a-113">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="4116a-113">Output : 'T[]</span></span>

<span data-ttu-id="4116a-114">Matriz sem elementos adjacentes iguais.</span><span class="sxs-lookup"><span data-stu-id="4116a-114">Array with no equal adjacent elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4116a-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4116a-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4116a-116">T'</span><span class="sxs-lookup"><span data-stu-id="4116a-116">'T</span></span>

<span data-ttu-id="4116a-117">O tipo de cada elemento de `array` .</span><span class="sxs-lookup"><span data-stu-id="4116a-117">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="4116a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4116a-118">Remarks</span></span>

<span data-ttu-id="4116a-119">Se houver vários elementos que são iguais, mas não próximos um do outro, haverá várias ocorrências na matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="4116a-119">If there are multiple elements that are equal but not next to each other, there will be multiple occurrences in the output array.</span></span>  <span data-ttu-id="4116a-120">Use essa função junto com `Sorted` para obter uma matriz com elementos exclusivos gerais.</span><span class="sxs-lookup"><span data-stu-id="4116a-120">Use this function together with `Sorted` to get an array with overall unique elements.</span></span>