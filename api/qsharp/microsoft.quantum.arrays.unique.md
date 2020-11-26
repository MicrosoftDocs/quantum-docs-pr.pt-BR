---
uid: Microsoft.Quantum.Arrays.Unique
title: Função Unique
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: 7964d5d41eb68cb05f9414164d69496c1f76eb08
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220001"
---
# <a name="unique-function"></a><span data-ttu-id="4f59d-102">Função Unique</span><span class="sxs-lookup"><span data-stu-id="4f59d-102">Unique function</span></span>

<span data-ttu-id="4f59d-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4f59d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4f59d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4f59d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4f59d-105">Retorna uma nova matriz que não tem nenhum elemento adjacente igual.</span><span class="sxs-lookup"><span data-stu-id="4f59d-105">Returns a new array that has no equal adjacent elements.</span></span>

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="4f59d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f59d-106">Description</span></span>

<span data-ttu-id="4f59d-107">Dada parte de uma matriz de elementos e uma função para testar a igualdade, essa função retorna uma nova matriz na qual a ordem relativa dos elementos é mantida, mas todos os elementos adjacentes que são iguais são filtrados para apenas um único elemento.</span><span class="sxs-lookup"><span data-stu-id="4f59d-107">Given some array of elements and a function to test equality, this function returns a new array in which the relative order of elements is kept, but all adjacent elements which are equal are filtered to just a single element.</span></span>

## <a name="input"></a><span data-ttu-id="4f59d-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f59d-108">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="4f59d-109">igual: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4f59d-109">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4f59d-110">Uma função que compara dois elementos, de modo que `a` é considerado igual a `b` If `equal(a, b)` is `true` .</span><span class="sxs-lookup"><span data-stu-id="4f59d-110">A function that compares two elements such that `a` is considered to be equal to `b` if `equal(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="4f59d-111">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="4f59d-111">array : 'T[]</span></span>

<span data-ttu-id="4f59d-112">A matriz a ser filtrada para elementos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="4f59d-112">The array to be filtered for unique elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="4f59d-113">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="4f59d-113">Output : 'T[]</span></span>

<span data-ttu-id="4f59d-114">Matriz sem elementos adjacentes iguais.</span><span class="sxs-lookup"><span data-stu-id="4f59d-114">Array with no equal adjacent elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4f59d-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4f59d-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4f59d-116">T'</span><span class="sxs-lookup"><span data-stu-id="4f59d-116">'T</span></span>

<span data-ttu-id="4f59d-117">O tipo de cada elemento de `array` .</span><span class="sxs-lookup"><span data-stu-id="4f59d-117">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f59d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f59d-118">Remarks</span></span>

<span data-ttu-id="4f59d-119">Se houver vários elementos que são iguais, mas não próximos um do outro, haverá várias ocorrências na matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="4f59d-119">If there are multiple elements that are equal but not next to each other, there will be multiple occurrences in the output array.</span></span>  <span data-ttu-id="4f59d-120">Use essa função junto com `Sorted` para obter uma matriz com elementos exclusivos gerais.</span><span class="sxs-lookup"><span data-stu-id="4f59d-120">Use this function together with `Sorted` to get an array with overall unique elements.</span></span>