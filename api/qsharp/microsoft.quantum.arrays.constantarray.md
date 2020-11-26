---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Função ConstantArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 8cba68af2f1e178a1ef96921283f85e4feb498ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210056"
---
# <a name="constantarray-function"></a><span data-ttu-id="d5840-102">Função ConstantArray</span><span class="sxs-lookup"><span data-stu-id="d5840-102">ConstantArray function</span></span>

<span data-ttu-id="d5840-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d5840-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d5840-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d5840-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d5840-105">Cria uma matriz de comprimento determinado com todos os elementos iguais ao valor fornecido.</span><span class="sxs-lookup"><span data-stu-id="d5840-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="d5840-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5840-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="d5840-107">comprimento: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d5840-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d5840-108">Comprimento da nova matriz.</span><span class="sxs-lookup"><span data-stu-id="d5840-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="d5840-109">valor: ' t</span><span class="sxs-lookup"><span data-stu-id="d5840-109">value : 'T</span></span>

<span data-ttu-id="d5840-110">O valor de cada elemento da nova matriz.</span><span class="sxs-lookup"><span data-stu-id="d5840-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="d5840-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="d5840-111">Output : 'T[]</span></span>

<span data-ttu-id="d5840-112">Uma nova matriz de comprimento `length` , de modo que cada elemento é `value` .</span><span class="sxs-lookup"><span data-stu-id="d5840-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d5840-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d5840-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d5840-114">T'</span><span class="sxs-lookup"><span data-stu-id="d5840-114">'T</span></span>

