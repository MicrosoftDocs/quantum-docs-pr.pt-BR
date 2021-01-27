---
uid: Microsoft.Quantum.Arrays.Tail
title: Função Tail
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Tail
qsharp.summary: Returns the last element of the array.
ms.openlocfilehash: 680562228a39263ef87ba053e6b7683412947e46
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845401"
---
# <a name="tail-function"></a><span data-ttu-id="0ea9a-102">Função Tail</span><span class="sxs-lookup"><span data-stu-id="0ea9a-102">Tail function</span></span>

<span data-ttu-id="0ea9a-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="0ea9a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="0ea9a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0ea9a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0ea9a-105">Retorna o último elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="0ea9a-105">Returns the last element of the array.</span></span>

```qsharp
function Tail<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="0ea9a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0ea9a-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="0ea9a-107">matriz: ' A []</span><span class="sxs-lookup"><span data-stu-id="0ea9a-107">array : 'A[]</span></span>

<span data-ttu-id="0ea9a-108">Matriz da qual o último elemento é tirado.</span><span class="sxs-lookup"><span data-stu-id="0ea9a-108">Array of which the last element is taken.</span></span> <span data-ttu-id="0ea9a-109">A matriz deve ter comprimento pelo menos 1.</span><span class="sxs-lookup"><span data-stu-id="0ea9a-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="0ea9a-110">Saída: ' A</span><span class="sxs-lookup"><span data-stu-id="0ea9a-110">Output : 'A</span></span>

<span data-ttu-id="0ea9a-111">O último elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="0ea9a-111">The last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0ea9a-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="0ea9a-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="0ea9a-113">' A</span><span class="sxs-lookup"><span data-stu-id="0ea9a-113">'A</span></span>

<span data-ttu-id="0ea9a-114">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="0ea9a-114">The type of the array elements.</span></span>