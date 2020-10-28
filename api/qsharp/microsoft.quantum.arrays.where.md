---
uid: Microsoft.Quantum.Arrays.Where
title: Função Where
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 1c9fa0463ed49788d12502257d735b965565d1ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694390"
---
# <a name="where-function"></a><span data-ttu-id="3723f-102">Função Where</span><span class="sxs-lookup"><span data-stu-id="3723f-102">Where function</span></span>

<span data-ttu-id="3723f-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3723f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3723f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3723f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3723f-105">Dado um predicado e uma matriz, retorna os índices dessa matriz em que o predicado é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="3723f-105">Given a predicate and an array, returns the indices of that array where the predicate is true.</span></span>

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="3723f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="3723f-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="3723f-107">predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool</span><span class="sxs-lookup"><span data-stu-id="3723f-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3723f-108">Uma função de `'T` para booliano que é usada para filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="3723f-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="3723f-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="3723f-109">array : 'T[]</span></span>

<span data-ttu-id="3723f-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="3723f-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="3723f-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3723f-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="3723f-112">Uma matriz de índices em que `predicate` é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="3723f-112">An array of indices where `predicate` is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3723f-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="3723f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3723f-114">T'</span><span class="sxs-lookup"><span data-stu-id="3723f-114">'T</span></span>

<span data-ttu-id="3723f-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="3723f-115">The type of `array` elements.</span></span>