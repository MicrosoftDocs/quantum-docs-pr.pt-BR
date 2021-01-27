---
uid: Microsoft.Quantum.Arrays.Merged
title: Função mesclada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: 262e7450188370212a7e2a57bf15e9f8ab162814
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845620"
---
# <a name="merged-function"></a><span data-ttu-id="6f62c-102">Função mesclada</span><span class="sxs-lookup"><span data-stu-id="6f62c-102">Merged function</span></span>

<span data-ttu-id="6f62c-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6f62c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6f62c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6f62c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6f62c-105">Dadas duas matrizes classificadas, retorna uma única matriz que contém os elementos de ambos na ordem classificada.</span><span class="sxs-lookup"><span data-stu-id="6f62c-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="6f62c-106">Usado internamente pela classificação de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="6f62c-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="6f62c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f62c-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="6f62c-108">comparação: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6f62c-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="6f62c-109">esquerda: ' t []</span><span class="sxs-lookup"><span data-stu-id="6f62c-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="6f62c-110">Right: ' t []</span><span class="sxs-lookup"><span data-stu-id="6f62c-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="6f62c-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="6f62c-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6f62c-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="6f62c-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6f62c-113">T'</span><span class="sxs-lookup"><span data-stu-id="6f62c-113">'T</span></span>

