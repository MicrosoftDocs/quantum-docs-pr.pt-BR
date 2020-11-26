---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Função prefixos
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 3501c11437534b1623bffba272a4517487e5634a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220375"
---
# <a name="prefixes-function"></a><span data-ttu-id="87f86-102">Função prefixos</span><span class="sxs-lookup"><span data-stu-id="87f86-102">Prefixes function</span></span>

<span data-ttu-id="87f86-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="87f86-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="87f86-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="87f86-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="87f86-105">Dada uma matriz, retorna todos os seus prefixos.</span><span class="sxs-lookup"><span data-stu-id="87f86-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="87f86-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="87f86-106">Description</span></span>

<span data-ttu-id="87f86-107">Retorna uma matriz de todos os prefixos, começando com uma matriz que só tem o primeiro elemento até a matriz completa.</span><span class="sxs-lookup"><span data-stu-id="87f86-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="87f86-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="87f86-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="87f86-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="87f86-109">array : 'T[]</span></span>

<span data-ttu-id="87f86-110">Uma matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="87f86-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="87f86-111">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="87f86-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="87f86-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="87f86-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="87f86-113">T'</span><span class="sxs-lookup"><span data-stu-id="87f86-113">'T</span></span>

<span data-ttu-id="87f86-114">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="87f86-114">The type of `array` elements.</span></span>