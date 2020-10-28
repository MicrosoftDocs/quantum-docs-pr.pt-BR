---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Função FunctionAsOperation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 90e9f0c922a77fbb6d6faf8945d4f5d1c8ff33b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693628"
---
# <a name="functionasoperation-function"></a><span data-ttu-id="59333-102">Função FunctionAsOperation</span><span class="sxs-lookup"><span data-stu-id="59333-102">FunctionAsOperation function</span></span>

<span data-ttu-id="59333-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="59333-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="59333-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="59333-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="59333-105">Converte funções em operações.</span><span class="sxs-lookup"><span data-stu-id="59333-105">Converts functions to operations.</span></span>

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a><span data-ttu-id="59333-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="59333-106">Description</span></span>

<span data-ttu-id="59333-107">Dada uma função, retorna uma operação que chama essa função e que não faz mais nada.</span><span class="sxs-lookup"><span data-stu-id="59333-107">Given a function, returns an operation which calls that function, and which does nothing else.</span></span>

## <a name="input"></a><span data-ttu-id="59333-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="59333-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="59333-109">FN: ' entrada-> ' saída</span><span class="sxs-lookup"><span data-stu-id="59333-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="59333-110">Uma função a ser convertida em uma operação.</span><span class="sxs-lookup"><span data-stu-id="59333-110">A function to be converted to an operation.</span></span>



## <a name="output--input--output"></a><span data-ttu-id="59333-111">Saída: ' entrada => ' saída</span><span class="sxs-lookup"><span data-stu-id="59333-111">Output : 'Input => 'Output</span></span> 

<span data-ttu-id="59333-112">Uma operação `op` que `op(input)` é idêntica a `fn(input)` para todos `input` .</span><span class="sxs-lookup"><span data-stu-id="59333-112">An operation `op` such that `op(input)` is identical to `fn(input)` for all `input`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="59333-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="59333-113">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="59333-114">' Entrada</span><span class="sxs-lookup"><span data-stu-id="59333-114">'Input</span></span>

<span data-ttu-id="59333-115">Tipo de entrada da função a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="59333-115">Input type of the function to be converted.</span></span>
### <a name="output"></a><span data-ttu-id="59333-116">' Saída</span><span class="sxs-lookup"><span data-stu-id="59333-116">'Output</span></span>

<span data-ttu-id="59333-117">Tipo de saída da função a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="59333-117">Output type of the function to be converted.</span></span>

## <a name="remarks"></a><span data-ttu-id="59333-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="59333-118">Remarks</span></span>

<span data-ttu-id="59333-119">Isso é útil principalmente para passar funções a funções ou operações que esperam uma operação como entrada.</span><span class="sxs-lookup"><span data-stu-id="59333-119">This is mainly useful for passing functions to functions or operations which expect an operation as input.</span></span>