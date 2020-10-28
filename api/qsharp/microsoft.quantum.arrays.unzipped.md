---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Função não compactada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 37c960dc5dbdb8099fbebe1ad63cb44ce642733c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694396"
---
# <a name="unzipped-function"></a><span data-ttu-id="b2018-102">Função não compactada</span><span class="sxs-lookup"><span data-stu-id="b2018-102">Unzipped function</span></span>

<span data-ttu-id="b2018-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b2018-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b2018-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b2018-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b2018-105">Dada uma matriz de 2 tuplas, retorna uma tupla de duas matrizes, cada uma contendo os elementos das tuplas da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="b2018-105">Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.</span></span>

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a><span data-ttu-id="b2018-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b2018-106">Input</span></span>

### <a name="arr--tu"></a><span data-ttu-id="b2018-107">arr: (t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="b2018-107">arr : ('T,'U)[]</span></span>

<span data-ttu-id="b2018-108">Uma matriz que contém 2 tuplas</span><span class="sxs-lookup"><span data-stu-id="b2018-108">An array containing 2-tuples</span></span>



## <a name="output--tu"></a><span data-ttu-id="b2018-109">Saída: (t [], ' U [])</span><span class="sxs-lookup"><span data-stu-id="b2018-109">Output : ('T[],'U[])</span></span>

<span data-ttu-id="b2018-110">Duas matrizes, a primeira que contém todos os primeiros elementos das tuplas de entrada, a segunda que contém todos os elementos de cada segundo das tuplas de entrada.</span><span class="sxs-lookup"><span data-stu-id="b2018-110">Two arrays, the first one containing all first elements of the input tuples, the second one containing all second elements of the input tuples.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b2018-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b2018-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b2018-112">T'</span><span class="sxs-lookup"><span data-stu-id="b2018-112">'T</span></span>

<span data-ttu-id="b2018-113">O tipo do primeiro elemento em cada tupla</span><span class="sxs-lookup"><span data-stu-id="b2018-113">The type of the first element in each tuple</span></span>
### <a name="u"></a><span data-ttu-id="b2018-114">' U</span><span class="sxs-lookup"><span data-stu-id="b2018-114">'U</span></span>

<span data-ttu-id="b2018-115">O tipo do segundo elemento em cada tupla</span><span class="sxs-lookup"><span data-stu-id="b2018-115">The type of the second element in each tuple</span></span>

## <a name="see-also"></a><span data-ttu-id="b2018-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b2018-116">See Also</span></span>

- [<span data-ttu-id="b2018-117">Microsoft.Quantum.Arrays.ZipPED</span><span class="sxs-lookup"><span data-stu-id="b2018-117">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)