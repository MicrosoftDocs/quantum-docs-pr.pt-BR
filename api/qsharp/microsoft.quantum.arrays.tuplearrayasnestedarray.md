---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Função TupleArrayAsNestedArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 51a35555080d1d2475fc1aa9e48e84c7c6f92c51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845387"
---
# <a name="tuplearrayasnestedarray-function"></a><span data-ttu-id="4cd13-102">Função TupleArrayAsNestedArray</span><span class="sxs-lookup"><span data-stu-id="4cd13-102">TupleArrayAsNestedArray function</span></span>

<span data-ttu-id="4cd13-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4cd13-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4cd13-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4cd13-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4cd13-105">Transforma uma lista de duas tuplas em uma matriz aninhada.</span><span class="sxs-lookup"><span data-stu-id="4cd13-105">Turns a list of 2-tuples into a nested array.</span></span>

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="4cd13-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4cd13-106">Input</span></span>

### <a name="tuplelist--tt"></a><span data-ttu-id="4cd13-107">tuplelist: (t, ' t) []</span><span class="sxs-lookup"><span data-stu-id="4cd13-107">tupleList : ('T,'T)[]</span></span>

<span data-ttu-id="4cd13-108">Lista de 2 tuplas a serem transformadas em uma matriz aninhada.</span><span class="sxs-lookup"><span data-stu-id="4cd13-108">List of 2-tuples to be turned into a nested array.</span></span>



## <a name="output--t"></a><span data-ttu-id="4cd13-109">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="4cd13-109">Output : 'T[][]</span></span>

<span data-ttu-id="4cd13-110">Uma matriz aninhada com comprimento correspondente à tuplalist.</span><span class="sxs-lookup"><span data-stu-id="4cd13-110">A nested array with length matching the tupleList.</span></span>

## <a name="example"></a><span data-ttu-id="4cd13-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4cd13-111">Example</span></span>

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a><span data-ttu-id="4cd13-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4cd13-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4cd13-113">T'</span><span class="sxs-lookup"><span data-stu-id="4cd13-113">'T</span></span>

