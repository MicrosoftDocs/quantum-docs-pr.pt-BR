---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Função RectangularArrayFact
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: b8ef7d52f7f815ca3e21ded1236e775a381646cb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220409"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="403ba-102">Função RectangularArrayFact</span><span class="sxs-lookup"><span data-stu-id="403ba-102">RectangularArrayFact function</span></span>

<span data-ttu-id="403ba-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="403ba-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="403ba-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="403ba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="403ba-105">Representa uma condição de que uma matriz bidimensional tem uma forma retangular</span><span class="sxs-lookup"><span data-stu-id="403ba-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="403ba-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="403ba-106">Description</span></span>

<span data-ttu-id="403ba-107">Essa função declara que cada linha em uma matriz tem o mesmo comprimento.</span><span class="sxs-lookup"><span data-stu-id="403ba-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="403ba-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="403ba-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="403ba-109">matriz: t [] []</span><span class="sxs-lookup"><span data-stu-id="403ba-109">array : 'T[][]</span></span>

<span data-ttu-id="403ba-110">Uma matriz bidimensional de elementos</span><span class="sxs-lookup"><span data-stu-id="403ba-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="403ba-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="403ba-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="403ba-112">Uma mensagem a ser impressa se a matriz não for uma matriz retangular</span><span class="sxs-lookup"><span data-stu-id="403ba-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="403ba-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="403ba-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="403ba-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="403ba-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="403ba-115">T'</span><span class="sxs-lookup"><span data-stu-id="403ba-115">'T</span></span>

<span data-ttu-id="403ba-116">O tipo de cada elemento de `array` .</span><span class="sxs-lookup"><span data-stu-id="403ba-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="403ba-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="403ba-117">See Also</span></span>

- [<span data-ttu-id="403ba-118">Microsoft. Quantum. arrays. SquareArrayFact</span><span class="sxs-lookup"><span data-stu-id="403ba-118">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)