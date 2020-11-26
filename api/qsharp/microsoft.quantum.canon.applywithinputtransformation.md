---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformation
title: Operação ApplyWithInputTransformation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformation
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 3586e9a114a550fb1989186e9c18fe4f344cf060
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217179"
---
# <a name="applywithinputtransformation-operation"></a><span data-ttu-id="d1ac9-102">Operação ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="d1ac9-102">ApplyWithInputTransformation operation</span></span>

<span data-ttu-id="d1ac9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d1ac9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d1ac9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d1ac9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d1ac9-105">Dada uma operação que aceita alguma entrada, uma função que retorna uma saída compatível com essa operação e uma entrada para essa função, aplica a operação usando a função para transformar a entrada em um formato esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="d1ac9-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit), input : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="d1ac9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1ac9-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="d1ac9-107">FN: ' U-> ' t</span><span class="sxs-lookup"><span data-stu-id="d1ac9-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="d1ac9-108">Uma função que transforma a entrada fornecida em um formulário esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="d1ac9-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="d1ac9-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="d1ac9-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d1ac9-110">A operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="d1ac9-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="d1ac9-111">entrada: ' U</span><span class="sxs-lookup"><span data-stu-id="d1ac9-111">input : 'U</span></span>

<span data-ttu-id="d1ac9-112">Uma entrada para a função.</span><span class="sxs-lookup"><span data-stu-id="d1ac9-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d1ac9-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d1ac9-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d1ac9-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d1ac9-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d1ac9-115">T'</span><span class="sxs-lookup"><span data-stu-id="d1ac9-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="d1ac9-116">' U</span><span class="sxs-lookup"><span data-stu-id="d1ac9-116">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="d1ac9-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d1ac9-117">See Also</span></span>

- [<span data-ttu-id="d1ac9-118">Microsoft. Quantum. Canon. ApplyWithInputTransformationA</span><span class="sxs-lookup"><span data-stu-id="d1ac9-118">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="d1ac9-119">Microsoft. Quantum. Canon. ApplyWithInputTransformationC</span><span class="sxs-lookup"><span data-stu-id="d1ac9-119">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="d1ac9-120">Microsoft. Quantum. Canon. ApplyWithInputTransformationCA</span><span class="sxs-lookup"><span data-stu-id="d1ac9-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="d1ac9-121">Microsoft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="d1ac9-121">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)