---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Função ConstantArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 848f18944829d08a10ec602dcb5d99c100c81f76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694500"
---
# <a name="constantarray-function"></a><span data-ttu-id="268dc-102">Função ConstantArray</span><span class="sxs-lookup"><span data-stu-id="268dc-102">ConstantArray function</span></span>

<span data-ttu-id="268dc-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="268dc-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="268dc-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="268dc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="268dc-105">Cria uma matriz de comprimento determinado com todos os elementos iguais ao valor fornecido.</span><span class="sxs-lookup"><span data-stu-id="268dc-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="268dc-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="268dc-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="268dc-107">comprimento: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="268dc-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="268dc-108">Comprimento da nova matriz.</span><span class="sxs-lookup"><span data-stu-id="268dc-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="268dc-109">valor: ' t</span><span class="sxs-lookup"><span data-stu-id="268dc-109">value : 'T</span></span>

<span data-ttu-id="268dc-110">O valor de cada elemento da nova matriz.</span><span class="sxs-lookup"><span data-stu-id="268dc-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="268dc-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="268dc-111">Output : 'T[]</span></span>

<span data-ttu-id="268dc-112">Uma nova matriz de comprimento `length` , de modo que cada elemento é `value` .</span><span class="sxs-lookup"><span data-stu-id="268dc-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="268dc-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="268dc-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="268dc-114">T'</span><span class="sxs-lookup"><span data-stu-id="268dc-114">'T</span></span>

