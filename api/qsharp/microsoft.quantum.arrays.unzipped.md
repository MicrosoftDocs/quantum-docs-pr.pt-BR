---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Função não compactada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 7eea7982721dc596b8660be5f3634df71b1ddf95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845375"
---
# <a name="unzipped-function"></a><span data-ttu-id="287d2-102">Função não compactada</span><span class="sxs-lookup"><span data-stu-id="287d2-102">Unzipped function</span></span>

<span data-ttu-id="287d2-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="287d2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="287d2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="287d2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="287d2-105">Dada uma matriz de 2 tuplas, retorna uma tupla de duas matrizes, cada uma contendo os elementos das tuplas da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="287d2-105">Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.</span></span>

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a><span data-ttu-id="287d2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="287d2-106">Input</span></span>

### <a name="arr--tu"></a><span data-ttu-id="287d2-107">arr: (t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="287d2-107">arr : ('T,'U)[]</span></span>

<span data-ttu-id="287d2-108">Uma matriz que contém 2 tuplas</span><span class="sxs-lookup"><span data-stu-id="287d2-108">An array containing 2-tuples</span></span>



## <a name="output--tu"></a><span data-ttu-id="287d2-109">Saída: (t [], ' U [])</span><span class="sxs-lookup"><span data-stu-id="287d2-109">Output : ('T[],'U[])</span></span>

<span data-ttu-id="287d2-110">Duas matrizes, a primeira que contém todos os primeiros elementos das tuplas de entrada, a segunda que contém todos os elementos de cada segundo das tuplas de entrada.</span><span class="sxs-lookup"><span data-stu-id="287d2-110">Two arrays, the first one containing all first elements of the input tuples, the second one containing all second elements of the input tuples.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="287d2-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="287d2-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="287d2-112">T'</span><span class="sxs-lookup"><span data-stu-id="287d2-112">'T</span></span>

<span data-ttu-id="287d2-113">O tipo do primeiro elemento em cada tupla</span><span class="sxs-lookup"><span data-stu-id="287d2-113">The type of the first element in each tuple</span></span>
### <a name="u"></a><span data-ttu-id="287d2-114">' U</span><span class="sxs-lookup"><span data-stu-id="287d2-114">'U</span></span>

<span data-ttu-id="287d2-115">O tipo do segundo elemento em cada tupla</span><span class="sxs-lookup"><span data-stu-id="287d2-115">The type of the second element in each tuple</span></span>

## <a name="example"></a><span data-ttu-id="287d2-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="287d2-116">Example</span></span>

```qsharp
// split is same as ([6, 5, 5, 3, 2, 1], [true, false, false, false, true, false])
let split = Unzipped([(6, true), (5, false), (5, false), (3, false), (2, true), (1, false)]);
```

## <a name="see-also"></a><span data-ttu-id="287d2-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="287d2-117">See Also</span></span>

- [<span data-ttu-id="287d2-118">Microsoft.Quantum.Arrays.ZipPED</span><span class="sxs-lookup"><span data-stu-id="287d2-118">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)