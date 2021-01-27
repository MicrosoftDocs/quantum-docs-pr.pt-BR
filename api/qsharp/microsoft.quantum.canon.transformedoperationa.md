---
uid: Microsoft.Quantum.Canon.TransformedOperationA
title: Função TransformedOperationA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: fac0fb6e03dc515892783fb4a5fa9cfc274550b8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840138"
---
# <a name="transformedoperationa-function"></a><span data-ttu-id="4fc7c-102">Função TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="4fc7c-102">TransformedOperationA function</span></span>

<span data-ttu-id="4fc7c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4fc7c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4fc7c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4fc7c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4fc7c-105">Dada uma função e uma operação, retorna uma nova operação cuja entrada é transformada pela função fornecida.</span><span class="sxs-lookup"><span data-stu-id="4fc7c-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj)) : ('U => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="4fc7c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4fc7c-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="4fc7c-107">FN: ' U-> ' t</span><span class="sxs-lookup"><span data-stu-id="4fc7c-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="4fc7c-108">Uma função que transforma a entrada fornecida em um formulário esperado pela operação.</span><span class="sxs-lookup"><span data-stu-id="4fc7c-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="4fc7c-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="4fc7c-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="4fc7c-110">A operação a ser transformada.</span><span class="sxs-lookup"><span data-stu-id="4fc7c-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-adj"></a><span data-ttu-id="4fc7c-111">Saída: ' U = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="4fc7c-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="4fc7c-112">Uma nova operação tbat chamadas `fn` com sua entrada e, em seguida, passa a saída resultante para `op` .</span><span class="sxs-lookup"><span data-stu-id="4fc7c-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4fc7c-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4fc7c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4fc7c-114">T'</span><span class="sxs-lookup"><span data-stu-id="4fc7c-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="4fc7c-115">' U</span><span class="sxs-lookup"><span data-stu-id="4fc7c-115">'U</span></span>



## <a name="example"></a><span data-ttu-id="4fc7c-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4fc7c-116">Example</span></span>

<span data-ttu-id="4fc7c-117">A chamada a seguir usa @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" para transformar uma operação projetada para @"Microsoft.Quantum.Arithmetic.BigEndian" entradas em uma operação que aceita entradas do tipo @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="4fc7c-117">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to transform an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs into an operation that accepts inputs of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a><span data-ttu-id="4fc7c-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4fc7c-118">See Also</span></span>

- [<span data-ttu-id="4fc7c-119">Microsoft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="4fc7c-119">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="4fc7c-120">Microsoft. Quantum. Canon. TransformedOperationC</span><span class="sxs-lookup"><span data-stu-id="4fc7c-120">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="4fc7c-121">Microsoft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="4fc7c-121">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="4fc7c-122">Microsoft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="4fc7c-122">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="4fc7c-123">Microsoft. Quantum. Canon. composto</span><span class="sxs-lookup"><span data-stu-id="4fc7c-123">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)