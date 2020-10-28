---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Função TupleArrayAsNestedArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 917f35db949790ab3ae6e7a2184bcfcf5ed50be6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694399"
---
# <a name="tuplearrayasnestedarray-function"></a><span data-ttu-id="665d2-102">Função TupleArrayAsNestedArray</span><span class="sxs-lookup"><span data-stu-id="665d2-102">TupleArrayAsNestedArray function</span></span>

<span data-ttu-id="665d2-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="665d2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="665d2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="665d2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="665d2-105">Transforma uma lista de duas tuplas em uma matriz aninhada.</span><span class="sxs-lookup"><span data-stu-id="665d2-105">Turns a list of 2-tuples into a nested array.</span></span>

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="665d2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="665d2-106">Input</span></span>

### <a name="tuplelist--tt"></a><span data-ttu-id="665d2-107">tuplelist: (t, ' t) []</span><span class="sxs-lookup"><span data-stu-id="665d2-107">tupleList : ('T,'T)[]</span></span>

<span data-ttu-id="665d2-108">Lista de 2 tuplas a serem transformadas em uma matriz aninhada.</span><span class="sxs-lookup"><span data-stu-id="665d2-108">List of 2-tuples to be turned into a nested array.</span></span>



## <a name="output--t"></a><span data-ttu-id="665d2-109">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="665d2-109">Output : 'T[][]</span></span>

<span data-ttu-id="665d2-110">Uma matriz aninhada com comprimento correspondente à tuplalist.</span><span class="sxs-lookup"><span data-stu-id="665d2-110">A nested array with length matching the tupleList.</span></span>

## <a name="example"></a><span data-ttu-id="665d2-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="665d2-111">Example</span></span>

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a><span data-ttu-id="665d2-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="665d2-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="665d2-113">T'</span><span class="sxs-lookup"><span data-stu-id="665d2-113">'T</span></span>

