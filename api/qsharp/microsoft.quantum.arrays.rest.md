---
uid: Microsoft.Quantum.Arrays.Rest
title: Função REST
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: c14e4b2902741d7ea70c895aa715cbcaa849af3e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694417"
---
# <a name="rest-function"></a><span data-ttu-id="a3755-102">Função REST</span><span class="sxs-lookup"><span data-stu-id="a3755-102">Rest function</span></span>

<span data-ttu-id="a3755-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a3755-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a3755-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a3755-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a3755-105">Cria uma matriz que é igual a uma matriz de entrada, exceto que o primeiro elemento da matriz é Descartado.</span><span class="sxs-lookup"><span data-stu-id="a3755-105">Creates an array that is equal to an input array except that the first array element is dropped.</span></span>

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="a3755-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3755-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="a3755-107">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="a3755-107">array : 'T[]</span></span>

<span data-ttu-id="a3755-108">Uma matriz cujo segundo para o último elementos é formar a matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="a3755-108">An array whose second to last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="a3755-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="a3755-109">Output : 'T[]</span></span>

<span data-ttu-id="a3755-110">Uma matriz que contém os elementos `array[1..Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="a3755-110">An array containing the elements `array[1..Length(array) - 1]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a3755-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a3755-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a3755-112">T'</span><span class="sxs-lookup"><span data-stu-id="a3755-112">'T</span></span>

<span data-ttu-id="a3755-113">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="a3755-113">The type of the array elements.</span></span>