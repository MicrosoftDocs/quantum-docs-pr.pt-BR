---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Função SquareArrayFact
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: f7f0573db9098feebfd481624e11119c58fd9eed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694407"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="d716a-102">Função SquareArrayFact</span><span class="sxs-lookup"><span data-stu-id="d716a-102">SquareArrayFact function</span></span>

<span data-ttu-id="d716a-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d716a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d716a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d716a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d716a-105">Representa uma condição de que uma matriz bidimensional tem uma forma quadrada</span><span class="sxs-lookup"><span data-stu-id="d716a-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="d716a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d716a-106">Description</span></span>

<span data-ttu-id="d716a-107">Essa função declara que cada linha em uma matriz tem tantos elementos quanto há linhas (elementos) na matriz.</span><span class="sxs-lookup"><span data-stu-id="d716a-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="d716a-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="d716a-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="d716a-109">matriz: t [] []</span><span class="sxs-lookup"><span data-stu-id="d716a-109">array : 'T[][]</span></span>

<span data-ttu-id="d716a-110">Uma matriz bidimensional de elementos</span><span class="sxs-lookup"><span data-stu-id="d716a-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="d716a-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="d716a-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="d716a-112">Uma mensagem a ser impressa se a matriz não for uma matriz quadrada</span><span class="sxs-lookup"><span data-stu-id="d716a-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="d716a-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d716a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d716a-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d716a-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d716a-115">T'</span><span class="sxs-lookup"><span data-stu-id="d716a-115">'T</span></span>

<span data-ttu-id="d716a-116">O tipo de cada elemento de `array` .</span><span class="sxs-lookup"><span data-stu-id="d716a-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="d716a-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d716a-117">See Also</span></span>

- [<span data-ttu-id="d716a-118">Microsoft. Quantum. arrays. RectangularArrayFact</span><span class="sxs-lookup"><span data-stu-id="d716a-118">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)