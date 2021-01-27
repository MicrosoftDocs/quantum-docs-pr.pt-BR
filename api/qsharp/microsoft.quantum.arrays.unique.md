---
uid: Microsoft.Quantum.Arrays.Unique
title: Função Unique
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: b3aa03d20195bdd8bb64783a9b68cafac29e68f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850917"
---
# <a name="unique-function"></a><span data-ttu-id="f0f56-102">Função Unique</span><span class="sxs-lookup"><span data-stu-id="f0f56-102">Unique function</span></span>

<span data-ttu-id="f0f56-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f0f56-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f0f56-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f0f56-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f0f56-105">Retorna uma nova matriz que não tem nenhum elemento adjacente igual.</span><span class="sxs-lookup"><span data-stu-id="f0f56-105">Returns a new array that has no equal adjacent elements.</span></span>

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="f0f56-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0f56-106">Description</span></span>

<span data-ttu-id="f0f56-107">Dada parte de uma matriz de elementos e uma função para testar a igualdade, essa função retorna uma nova matriz na qual a ordem relativa dos elementos é mantida, mas todos os elementos adjacentes que são iguais são filtrados para apenas um único elemento.</span><span class="sxs-lookup"><span data-stu-id="f0f56-107">Given some array of elements and a function to test equality, this function returns a new array in which the relative order of elements is kept, but all adjacent elements which are equal are filtered to just a single element.</span></span>

## <a name="input"></a><span data-ttu-id="f0f56-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0f56-108">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="f0f56-109">igual: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f0f56-109">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f0f56-110">Uma função que compara dois elementos, de modo que `a` é considerado igual a `b` If `equal(a, b)` is `true` .</span><span class="sxs-lookup"><span data-stu-id="f0f56-110">A function that compares two elements such that `a` is considered to be equal to `b` if `equal(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="f0f56-111">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="f0f56-111">array : 'T[]</span></span>

<span data-ttu-id="f0f56-112">A matriz a ser filtrada para elementos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f0f56-112">The array to be filtered for unique elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="f0f56-113">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="f0f56-113">Output : 'T[]</span></span>

<span data-ttu-id="f0f56-114">Matriz sem elementos adjacentes iguais.</span><span class="sxs-lookup"><span data-stu-id="f0f56-114">Array with no equal adjacent elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f0f56-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f0f56-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f0f56-116">T'</span><span class="sxs-lookup"><span data-stu-id="f0f56-116">'T</span></span>

<span data-ttu-id="f0f56-117">O tipo de cada elemento de `array` .</span><span class="sxs-lookup"><span data-stu-id="f0f56-117">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="f0f56-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f0f56-118">Example</span></span>

```qsharp
let unique1 = Unique(EqualI, [1, 1, 3, 3, 2, 5, 5, 5, 7]);
// same as [1, 3, 2, 5, 7]
let unique2 = Unique(EqualI, [2, 2, 1, 1, 2, 2, 1, 1]);
// same as [2, 1, 2, 1];
let unique3 = Unique(EqualI, Sorted(LessThanOrEqualI, [2, 2, 1, 1, 2, 2, 1, 1]));
// same as [1, 2];
```

## <a name="remarks"></a><span data-ttu-id="f0f56-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0f56-119">Remarks</span></span>

<span data-ttu-id="f0f56-120">Se houver vários elementos que são iguais, mas não próximos um do outro, haverá várias ocorrências na matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="f0f56-120">If there are multiple elements that are equal but not next to each other, there will be multiple occurrences in the output array.</span></span>  <span data-ttu-id="f0f56-121">Use essa função junto com `Sorted` para obter uma matriz com elementos exclusivos gerais.</span><span class="sxs-lookup"><span data-stu-id="f0f56-121">Use this function together with `Sorted` to get an array with overall unique elements.</span></span>