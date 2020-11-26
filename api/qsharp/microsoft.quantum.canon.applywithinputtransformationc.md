---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationC
title: Operação ApplyWithInputTransformationC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationC
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 030c41d3ce0a5d613a95c6511f7278497ec5cda1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217162"
---
# <a name="applywithinputtransformationc-operation"></a><span data-ttu-id="f2eec-102">Operação ApplyWithInputTransformationC</span><span class="sxs-lookup"><span data-stu-id="f2eec-102">ApplyWithInputTransformationC operation</span></span>

<span data-ttu-id="f2eec-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f2eec-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f2eec-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f2eec-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f2eec-105">Dada uma operação que aceita alguma entrada, uma função que retorna uma saída compatível com essa operação e uma entrada para essa função, aplica a operação usando a função para transformar a entrada em um formato esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="f2eec-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl), input : 'U) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="f2eec-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f2eec-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="f2eec-107">FN: ' U-> ' t</span><span class="sxs-lookup"><span data-stu-id="f2eec-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="f2eec-108">Uma função que transforma a entrada fornecida em um formulário esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="f2eec-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="f2eec-109">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="f2eec-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="f2eec-110">A operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="f2eec-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="f2eec-111">entrada: ' U</span><span class="sxs-lookup"><span data-stu-id="f2eec-111">input : 'U</span></span>

<span data-ttu-id="f2eec-112">Uma entrada para a função.</span><span class="sxs-lookup"><span data-stu-id="f2eec-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f2eec-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f2eec-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f2eec-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f2eec-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f2eec-115">T'</span><span class="sxs-lookup"><span data-stu-id="f2eec-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="f2eec-116">' U</span><span class="sxs-lookup"><span data-stu-id="f2eec-116">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="f2eec-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f2eec-117">See Also</span></span>

- [<span data-ttu-id="f2eec-118">Microsoft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="f2eec-118">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="f2eec-119">Microsoft. Quantum. Canon. ApplyWithInputTransformationA</span><span class="sxs-lookup"><span data-stu-id="f2eec-119">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="f2eec-120">Microsoft. Quantum. Canon. ApplyWithInputTransformationCA</span><span class="sxs-lookup"><span data-stu-id="f2eec-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="f2eec-121">Microsoft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="f2eec-121">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)