---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: Função TransformedOperationCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: bb39530ae28e17d07a6a5c2bb2d35f81be312d15
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840116"
---
# <a name="transformedoperationca-function"></a><span data-ttu-id="9d604-102">Função TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="9d604-102">TransformedOperationCA function</span></span>

<span data-ttu-id="9d604-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9d604-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9d604-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9d604-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9d604-105">Dada uma função e uma operação, retorna uma nova operação cuja entrada é transformada pela função fornecida.</span><span class="sxs-lookup"><span data-stu-id="9d604-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="9d604-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="9d604-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="9d604-107">FN: ' U-> ' t</span><span class="sxs-lookup"><span data-stu-id="9d604-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="9d604-108">Uma função que transforma a entrada fornecida em um formulário esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="9d604-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="9d604-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="9d604-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="9d604-110">A operação a ser transformada.</span><span class="sxs-lookup"><span data-stu-id="9d604-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-adj--ctl"></a><span data-ttu-id="9d604-111">Saída: "U => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="9d604-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="9d604-112">Uma nova operação tbat chamadas `fn` com sua entrada e, em seguida, passa a saída resultante para `op` .</span><span class="sxs-lookup"><span data-stu-id="9d604-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9d604-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="9d604-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9d604-114">T'</span><span class="sxs-lookup"><span data-stu-id="9d604-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="9d604-115">' U</span><span class="sxs-lookup"><span data-stu-id="9d604-115">'U</span></span>



## <a name="example"></a><span data-ttu-id="9d604-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9d604-116">Example</span></span>

<span data-ttu-id="9d604-117">A chamada a seguir usa @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" para transformar uma operação projetada para @"Microsoft.Quantum.Arithmetic.BigEndian" entradas em uma operação que aceita entradas do tipo @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="9d604-117">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to transform an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs into an operation that accepts inputs of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a><span data-ttu-id="9d604-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9d604-118">See Also</span></span>

- [<span data-ttu-id="9d604-119">Microsoft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="9d604-119">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="9d604-120">Microsoft. Quantum. Canon. TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="9d604-120">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="9d604-121">Microsoft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="9d604-121">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="9d604-122">Microsoft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="9d604-122">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="9d604-123">Microsoft. Quantum. Canon. composto</span><span class="sxs-lookup"><span data-stu-id="9d604-123">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)