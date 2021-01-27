---
uid: Microsoft.Quantum.Arrays.IndexOf
title: Função IndexOf
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 64db55e831078a7130a3ced6a30bfbd2299c392d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848519"
---
# <a name="indexof-function"></a><span data-ttu-id="25dc1-102">Função IndexOf</span><span class="sxs-lookup"><span data-stu-id="25dc1-102">IndexOf function</span></span>

<span data-ttu-id="25dc1-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="25dc1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="25dc1-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25dc1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25dc1-105">Retorna o primeiro índice do primeiro elemento em uma matriz que atende a um determinado predicado.</span><span class="sxs-lookup"><span data-stu-id="25dc1-105">Returns the first index of the first element in an array that satisfies a given predicate.</span></span> <span data-ttu-id="25dc1-106">Se nenhum elemento desse tipo existir, retornará-1.</span><span class="sxs-lookup"><span data-stu-id="25dc1-106">If no such element exists, returns -1.</span></span>

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="25dc1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="25dc1-107">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="25dc1-108">predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool</span><span class="sxs-lookup"><span data-stu-id="25dc1-108">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="25dc1-109">Uma função de predicado agindo em elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="25dc1-109">A predicate function acting on elements of the array.</span></span>


### <a name="arr--t"></a><span data-ttu-id="25dc1-110">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="25dc1-110">arr : 'T[]</span></span>

<span data-ttu-id="25dc1-111">Uma matriz a ser pesquisada usando o predicado fornecido.</span><span class="sxs-lookup"><span data-stu-id="25dc1-111">An array to be searched using the given predicate.</span></span>



## <a name="output--int"></a><span data-ttu-id="25dc1-112">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="25dc1-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="25dc1-113">O menor índice `idx` , como `predicate(arr[idx])` true, ou-1, se nenhum elemento desse tipo existir.</span><span class="sxs-lookup"><span data-stu-id="25dc1-113">Either the smallest index `idx` such that `predicate(arr[idx])` is true, or -1 if no such element exists.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="25dc1-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="25dc1-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="25dc1-115">T'</span><span class="sxs-lookup"><span data-stu-id="25dc1-115">'T</span></span>



## <a name="example"></a><span data-ttu-id="25dc1-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="25dc1-116">Example</span></span>

<span data-ttu-id="25dc1-117">Suponha que `IsEven : Int -> Bool` seja uma função que retorna `true` se e somente se sua entrada for par.</span><span class="sxs-lookup"><span data-stu-id="25dc1-117">Suppose that `IsEven : Int -> Bool` is a function that returns `true` if and only if its input is even.</span></span> <span data-ttu-id="25dc1-118">Em seguida, isso pode ser usado com `IndexOf` para localizar o primeiro elemento par em uma matriz:</span><span class="sxs-lookup"><span data-stu-id="25dc1-118">Then, this can be used with `IndexOf` to find the first even element in an array:</span></span>

```qsharp
let items = [1, 3, 17, 2, 21];
let idx = IndexOf(IsEven, items); // returns 3
```