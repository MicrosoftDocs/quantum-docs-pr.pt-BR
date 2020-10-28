---
uid: Microsoft.Quantum.Arrays.Merged
title: Função mesclada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: da15a36f8f057cdc15062c96070ec21becc4794a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694433"
---
# <a name="merged-function"></a><span data-ttu-id="cc161-102">Função mesclada</span><span class="sxs-lookup"><span data-stu-id="cc161-102">Merged function</span></span>

<span data-ttu-id="cc161-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="cc161-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="cc161-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cc161-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cc161-105">Dadas duas matrizes classificadas, retorna uma única matriz que contém os elementos de ambos na ordem classificada.</span><span class="sxs-lookup"><span data-stu-id="cc161-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="cc161-106">Usado internamente pela classificação de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="cc161-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="cc161-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc161-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="cc161-108">comparação: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cc161-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="cc161-109">esquerda: ' t []</span><span class="sxs-lookup"><span data-stu-id="cc161-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="cc161-110">Right: ' t []</span><span class="sxs-lookup"><span data-stu-id="cc161-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="cc161-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="cc161-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cc161-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="cc161-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cc161-113">T'</span><span class="sxs-lookup"><span data-stu-id="cc161-113">'T</span></span>

