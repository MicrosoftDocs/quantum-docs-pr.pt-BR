---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Função prefixos
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 1576e57e9dc64a605eb65cb841640e72a3b126ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694421"
---
# <a name="prefixes-function"></a><span data-ttu-id="83d51-102">Função prefixos</span><span class="sxs-lookup"><span data-stu-id="83d51-102">Prefixes function</span></span>

<span data-ttu-id="83d51-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="83d51-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="83d51-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="83d51-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="83d51-105">Dada uma matriz, retorna todos os seus prefixos.</span><span class="sxs-lookup"><span data-stu-id="83d51-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="83d51-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="83d51-106">Description</span></span>

<span data-ttu-id="83d51-107">Retorna uma matriz de todos os prefixos, começando com uma matriz que só tem o primeiro elemento até a matriz completa.</span><span class="sxs-lookup"><span data-stu-id="83d51-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="83d51-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="83d51-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="83d51-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="83d51-109">array : 'T[]</span></span>

<span data-ttu-id="83d51-110">Uma matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="83d51-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="83d51-111">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="83d51-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="83d51-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="83d51-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="83d51-113">T'</span><span class="sxs-lookup"><span data-stu-id="83d51-113">'T</span></span>

<span data-ttu-id="83d51-114">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="83d51-114">The type of `array` elements.</span></span>