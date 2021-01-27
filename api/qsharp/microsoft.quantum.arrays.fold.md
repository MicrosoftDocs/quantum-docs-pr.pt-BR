---
uid: Microsoft.Quantum.Arrays.Fold
title: Função de dobra
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: d12e070058178ce2cbdd70cade5bc16607a55d5e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848598"
---
# <a name="fold-function"></a><span data-ttu-id="c8408-102">Função de dobra</span><span class="sxs-lookup"><span data-stu-id="c8408-102">Fold function</span></span>

<span data-ttu-id="c8408-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c8408-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c8408-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c8408-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c8408-105">Itera uma função `f` por meio de uma matriz `array` , retornando `f(f(f(initialState, array[0]), array[1]), ...)` .</span><span class="sxs-lookup"><span data-stu-id="c8408-105">Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.</span></span>

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a><span data-ttu-id="c8408-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8408-106">Input</span></span>

### <a name="folder--statet---state"></a><span data-ttu-id="c8408-107">pasta: (' State, ' t)-estado de ></span><span class="sxs-lookup"><span data-stu-id="c8408-107">folder : ('State,'T) -> 'State</span></span>

<span data-ttu-id="c8408-108">Uma função a ser dobrada sobre a matriz.</span><span class="sxs-lookup"><span data-stu-id="c8408-108">A function to be folded over the array.</span></span>


### <a name="state--state"></a><span data-ttu-id="c8408-109">Estado: ' estado</span><span class="sxs-lookup"><span data-stu-id="c8408-109">state : 'State</span></span>

<span data-ttu-id="c8408-110">O estado inicial da pasta.</span><span class="sxs-lookup"><span data-stu-id="c8408-110">The initial state of the folder.</span></span>


### <a name="array--t"></a><span data-ttu-id="c8408-111">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="c8408-111">array : 'T[]</span></span>

<span data-ttu-id="c8408-112">Uma matriz de valores a serem dobrados.</span><span class="sxs-lookup"><span data-stu-id="c8408-112">An array of values to be folded over.</span></span>



## <a name="output--state"></a><span data-ttu-id="c8408-113">Saída: ' estado</span><span class="sxs-lookup"><span data-stu-id="c8408-113">Output : 'State</span></span>

<span data-ttu-id="c8408-114">O estado final retornado pela pasta após a iteração em todos os elementos de `array` .</span><span class="sxs-lookup"><span data-stu-id="c8408-114">The final state returned by the folder after iterating over all elements of `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c8408-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="c8408-115">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="c8408-116">' Estado</span><span class="sxs-lookup"><span data-stu-id="c8408-116">'State</span></span>

<span data-ttu-id="c8408-117">O tipo de Estados em que a `folder` função Opera, ou seja, aceita como seu primeiro argumento e retorna.</span><span class="sxs-lookup"><span data-stu-id="c8408-117">The type of states the `folder` function operates on, i.e., accepts as its first argument and returns.</span></span>
### <a name="t"></a><span data-ttu-id="c8408-118">T'</span><span class="sxs-lookup"><span data-stu-id="c8408-118">'T</span></span>

<span data-ttu-id="c8408-119">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="c8408-119">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="c8408-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c8408-120">Example</span></span>

```qsharp
function Plus(a : Double, b : Double) {
    return a + b;
}
function Sum(xs : Double[]) {
    return Fold(Plus, 0.0, xs);
}
```