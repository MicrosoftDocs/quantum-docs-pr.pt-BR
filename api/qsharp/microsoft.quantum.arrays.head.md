---
uid: Microsoft.Quantum.Arrays.Head
title: Função Head
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 834cbe2384122463be6a0efcb6e09785aae9c092
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221106"
---
# <a name="head-function"></a><span data-ttu-id="85118-102">Função Head</span><span class="sxs-lookup"><span data-stu-id="85118-102">Head function</span></span>

<span data-ttu-id="85118-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="85118-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="85118-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85118-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85118-105">Retorna o primeiro elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="85118-105">Returns the first element of the array.</span></span>

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="85118-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="85118-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="85118-107">matriz: ' A []</span><span class="sxs-lookup"><span data-stu-id="85118-107">array : 'A[]</span></span>

<span data-ttu-id="85118-108">Matriz da qual o primeiro elemento é tirado.</span><span class="sxs-lookup"><span data-stu-id="85118-108">Array of which the first element is taken.</span></span> <span data-ttu-id="85118-109">A matriz deve ter comprimento pelo menos 1.</span><span class="sxs-lookup"><span data-stu-id="85118-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="85118-110">Saída: ' A</span><span class="sxs-lookup"><span data-stu-id="85118-110">Output : 'A</span></span>

<span data-ttu-id="85118-111">O primeiro elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="85118-111">The first element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="85118-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="85118-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="85118-113">' A</span><span class="sxs-lookup"><span data-stu-id="85118-113">'A</span></span>

<span data-ttu-id="85118-114">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="85118-114">The type of the array elements.</span></span>