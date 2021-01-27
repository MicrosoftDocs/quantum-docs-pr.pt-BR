---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationA
title: Operação ApplyWithInputTransformationA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 3ab07f301f310e3ec380981bdb53201fc74bd289
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841133"
---
# <a name="applywithinputtransformationa-operation"></a><span data-ttu-id="14ec3-102">Operação ApplyWithInputTransformationA</span><span class="sxs-lookup"><span data-stu-id="14ec3-102">ApplyWithInputTransformationA operation</span></span>

<span data-ttu-id="14ec3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="14ec3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="14ec3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="14ec3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="14ec3-105">Dada uma operação que aceita alguma entrada, uma função que retorna uma saída compatível com essa operação e uma entrada para essa função, aplica a operação usando a função para transformar a entrada em um formato esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="14ec3-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj), input : 'U) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="14ec3-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="14ec3-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="14ec3-107">FN: ' U-> ' t</span><span class="sxs-lookup"><span data-stu-id="14ec3-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="14ec3-108">Uma função que transforma a entrada fornecida em um formulário esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="14ec3-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="14ec3-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="14ec3-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="14ec3-110">A operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="14ec3-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="14ec3-111">entrada: ' U</span><span class="sxs-lookup"><span data-stu-id="14ec3-111">input : 'U</span></span>

<span data-ttu-id="14ec3-112">Uma entrada para a função.</span><span class="sxs-lookup"><span data-stu-id="14ec3-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="14ec3-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="14ec3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="14ec3-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="14ec3-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="14ec3-115">T'</span><span class="sxs-lookup"><span data-stu-id="14ec3-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="14ec3-116">' U</span><span class="sxs-lookup"><span data-stu-id="14ec3-116">'U</span></span>



## <a name="example"></a><span data-ttu-id="14ec3-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="14ec3-117">Example</span></span>

<span data-ttu-id="14ec3-118">A chamada a seguir usa @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" para aplicar uma operação projetada para @"Microsoft.Quantum.Arithmetic.BigEndian" entradas a uma entrada do tipo @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="14ec3-118">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to apply an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs to an input of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a><span data-ttu-id="14ec3-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="14ec3-119">See Also</span></span>

- [<span data-ttu-id="14ec3-120">Microsoft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="14ec3-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="14ec3-121">Microsoft. Quantum. Canon. ApplyWithInputTransformationC</span><span class="sxs-lookup"><span data-stu-id="14ec3-121">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="14ec3-122">Microsoft. Quantum. Canon. ApplyWithInputTransformationCA</span><span class="sxs-lookup"><span data-stu-id="14ec3-122">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="14ec3-123">Microsoft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="14ec3-123">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)