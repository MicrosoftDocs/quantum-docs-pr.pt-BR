---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Função SquareArrayFact
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: a154e5becba4dae762596a3fc1b268855520fa1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850974"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="c83a1-102">Função SquareArrayFact</span><span class="sxs-lookup"><span data-stu-id="c83a1-102">SquareArrayFact function</span></span>

<span data-ttu-id="c83a1-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c83a1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c83a1-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c83a1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c83a1-105">Representa uma condição de que uma matriz bidimensional tem uma forma quadrada</span><span class="sxs-lookup"><span data-stu-id="c83a1-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="c83a1-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c83a1-106">Description</span></span>

<span data-ttu-id="c83a1-107">Essa função declara que cada linha em uma matriz tem tantos elementos quanto há linhas (elementos) na matriz.</span><span class="sxs-lookup"><span data-stu-id="c83a1-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="c83a1-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="c83a1-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="c83a1-109">matriz: t [] []</span><span class="sxs-lookup"><span data-stu-id="c83a1-109">array : 'T[][]</span></span>

<span data-ttu-id="c83a1-110">Uma matriz bidimensional de elementos</span><span class="sxs-lookup"><span data-stu-id="c83a1-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="c83a1-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="c83a1-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="c83a1-112">Uma mensagem a ser impressa se a matriz não for uma matriz quadrada</span><span class="sxs-lookup"><span data-stu-id="c83a1-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="c83a1-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c83a1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c83a1-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="c83a1-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c83a1-115">T'</span><span class="sxs-lookup"><span data-stu-id="c83a1-115">'T</span></span>

<span data-ttu-id="c83a1-116">O tipo de cada elemento de `array` .</span><span class="sxs-lookup"><span data-stu-id="c83a1-116">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="c83a1-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c83a1-117">Example</span></span>

```qsharp
SquareArrayFact([[1, 2], [3, 4]], "Array is not a square");       // okay
SquareArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not a square"); // will fail
SquareArrayFact([[1, 2], [3, 4, 5]], "Array is not a square");    // will fail
```

## <a name="see-also"></a><span data-ttu-id="c83a1-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c83a1-118">See Also</span></span>

- [<span data-ttu-id="c83a1-119">Microsoft. Quantum. arrays. RectangularArrayFact</span><span class="sxs-lookup"><span data-stu-id="c83a1-119">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)