---
uid: Microsoft.Quantum.Arrays.Swapped
title: Função permutada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: 575d6b76e52f198d91ab5557ada8032df491cfa3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850943"
---
# <a name="swapped-function"></a><span data-ttu-id="07c82-102">Função permutada</span><span class="sxs-lookup"><span data-stu-id="07c82-102">Swapped function</span></span>

<span data-ttu-id="07c82-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="07c82-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="07c82-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="07c82-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="07c82-105">Aplica uma troca de dois elementos em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="07c82-105">Applies a swap of two elements in an array.</span></span>

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="07c82-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="07c82-106">Input</span></span>

### <a name="firstindex--int"></a><span data-ttu-id="07c82-107">firstIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="07c82-107">firstIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="07c82-108">Índice do primeiro elemento a ser trocado.</span><span class="sxs-lookup"><span data-stu-id="07c82-108">Index of the first element to be swapped.</span></span>


### <a name="secondindex--int"></a><span data-ttu-id="07c82-109">secondIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="07c82-109">secondIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="07c82-110">Índice do segundo elemento a ser trocado.</span><span class="sxs-lookup"><span data-stu-id="07c82-110">Index of the second element to be swapped.</span></span>


### <a name="arr--t"></a><span data-ttu-id="07c82-111">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="07c82-111">arr : 'T[]</span></span>

<span data-ttu-id="07c82-112">Matriz com elementos a serem trocados.</span><span class="sxs-lookup"><span data-stu-id="07c82-112">Array with elements to be swapped.</span></span>



## <a name="output--t"></a><span data-ttu-id="07c82-113">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="07c82-113">Output : 'T[]</span></span>

<span data-ttu-id="07c82-114">A matriz com a permuta in loco aplicada.</span><span class="sxs-lookup"><span data-stu-id="07c82-114">The array with the in place swap applied.</span></span>

## <a name="example"></a><span data-ttu-id="07c82-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="07c82-115">Example</span></span>

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a><span data-ttu-id="07c82-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="07c82-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="07c82-117">T'</span><span class="sxs-lookup"><span data-stu-id="07c82-117">'T</span></span>

