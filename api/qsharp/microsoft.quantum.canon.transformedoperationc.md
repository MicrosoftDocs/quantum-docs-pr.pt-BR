---
uid: Microsoft.Quantum.Canon.TransformedOperationC
title: Função TransformedOperationC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationC
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 9475c5a1cc3b7e14c56c301749311a72e15f71e0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852039"
---
# <a name="transformedoperationc-function"></a><span data-ttu-id="2bf0a-102">Função TransformedOperationC</span><span class="sxs-lookup"><span data-stu-id="2bf0a-102">TransformedOperationC function</span></span>

<span data-ttu-id="2bf0a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2bf0a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2bf0a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2bf0a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2bf0a-105">Dada uma função e uma operação, retorna uma nova operação cuja entrada é transformada pela função fornecida.</span><span class="sxs-lookup"><span data-stu-id="2bf0a-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl)) : ('U => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="2bf0a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2bf0a-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="2bf0a-107">FN: ' U-> ' t</span><span class="sxs-lookup"><span data-stu-id="2bf0a-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="2bf0a-108">Uma função que transforma a entrada fornecida em um formulário esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="2bf0a-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="2bf0a-109">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="2bf0a-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="2bf0a-110">A operação a ser transformada.</span><span class="sxs-lookup"><span data-stu-id="2bf0a-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-ctl"></a><span data-ttu-id="2bf0a-111">Saída: "U => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL</span><span class="sxs-lookup"><span data-stu-id="2bf0a-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="2bf0a-112">Uma nova operação tbat chamadas `fn` com sua entrada e, em seguida, passa a saída resultante para `op` .</span><span class="sxs-lookup"><span data-stu-id="2bf0a-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2bf0a-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="2bf0a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2bf0a-114">T'</span><span class="sxs-lookup"><span data-stu-id="2bf0a-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="2bf0a-115">' U</span><span class="sxs-lookup"><span data-stu-id="2bf0a-115">'U</span></span>



## <a name="example"></a><span data-ttu-id="2bf0a-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2bf0a-116">Example</span></span>

<span data-ttu-id="2bf0a-117">A chamada a seguir usa @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" para transformar uma operação projetada para @"Microsoft.Quantum.Arithmetic.BigEndian" entradas em uma operação que aceita entradas do tipo @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="2bf0a-117">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to transform an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs into an operation that accepts inputs of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a><span data-ttu-id="2bf0a-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2bf0a-118">See Also</span></span>

- [<span data-ttu-id="2bf0a-119">Microsoft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="2bf0a-119">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="2bf0a-120">Microsoft. Quantum. Canon. TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="2bf0a-120">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="2bf0a-121">Microsoft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="2bf0a-121">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="2bf0a-122">Microsoft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="2bf0a-122">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="2bf0a-123">Microsoft. Quantum. Canon. composto</span><span class="sxs-lookup"><span data-stu-id="2bf0a-123">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)