---
uid: Microsoft.Quantum.Arrays.Rest
title: Função REST
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: b6c579df354185a2defb08cd78bce816d8cc5959
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845469"
---
# <a name="rest-function"></a><span data-ttu-id="a35f4-102">Função REST</span><span class="sxs-lookup"><span data-stu-id="a35f4-102">Rest function</span></span>

<span data-ttu-id="a35f4-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a35f4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a35f4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a35f4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a35f4-105">Cria uma matriz que é igual a uma matriz de entrada, exceto que o primeiro elemento da matriz é Descartado.</span><span class="sxs-lookup"><span data-stu-id="a35f4-105">Creates an array that is equal to an input array except that the first array element is dropped.</span></span>

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="a35f4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a35f4-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="a35f4-107">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="a35f4-107">array : 'T[]</span></span>

<span data-ttu-id="a35f4-108">Uma matriz cujo segundo para o último elementos é formar a matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="a35f4-108">An array whose second to last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="a35f4-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="a35f4-109">Output : 'T[]</span></span>

<span data-ttu-id="a35f4-110">Uma matriz que contém os elementos `array[1..Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="a35f4-110">An array containing the elements `array[1..Length(array) - 1]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a35f4-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a35f4-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a35f4-112">T'</span><span class="sxs-lookup"><span data-stu-id="a35f4-112">'T</span></span>

<span data-ttu-id="a35f4-113">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="a35f4-113">The type of the array elements.</span></span>