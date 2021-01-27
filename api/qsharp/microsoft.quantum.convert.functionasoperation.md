---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Função FunctionAsOperation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: cf4f8c97bf38b3a64eb952d0a502bc21c29c579c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833834"
---
# <a name="functionasoperation-function"></a><span data-ttu-id="8899e-102">Função FunctionAsOperation</span><span class="sxs-lookup"><span data-stu-id="8899e-102">FunctionAsOperation function</span></span>

<span data-ttu-id="8899e-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="8899e-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="8899e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8899e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8899e-105">Converte funções em operações.</span><span class="sxs-lookup"><span data-stu-id="8899e-105">Converts functions to operations.</span></span>

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a><span data-ttu-id="8899e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="8899e-106">Description</span></span>

<span data-ttu-id="8899e-107">Dada uma função, retorna uma operação que chama essa função e que não faz mais nada.</span><span class="sxs-lookup"><span data-stu-id="8899e-107">Given a function, returns an operation which calls that function, and which does nothing else.</span></span>

## <a name="input"></a><span data-ttu-id="8899e-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="8899e-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="8899e-109">FN: ' entrada-> ' saída</span><span class="sxs-lookup"><span data-stu-id="8899e-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="8899e-110">Uma função a ser convertida em uma operação.</span><span class="sxs-lookup"><span data-stu-id="8899e-110">A function to be converted to an operation.</span></span>



## <a name="output--input--output"></a><span data-ttu-id="8899e-111">Saída: ' entrada => ' saída</span><span class="sxs-lookup"><span data-stu-id="8899e-111">Output : 'Input => 'Output</span></span> 

<span data-ttu-id="8899e-112">Uma operação `op` que `op(input)` é idêntica a `fn(input)` para todos `input` .</span><span class="sxs-lookup"><span data-stu-id="8899e-112">An operation `op` such that `op(input)` is identical to `fn(input)` for all `input`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8899e-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="8899e-113">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="8899e-114">' Entrada</span><span class="sxs-lookup"><span data-stu-id="8899e-114">'Input</span></span>

<span data-ttu-id="8899e-115">Tipo de entrada da função a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="8899e-115">Input type of the function to be converted.</span></span>
### <a name="output"></a><span data-ttu-id="8899e-116">' Saída</span><span class="sxs-lookup"><span data-stu-id="8899e-116">'Output</span></span>

<span data-ttu-id="8899e-117">Tipo de saída da função a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="8899e-117">Output type of the function to be converted.</span></span>

## <a name="remarks"></a><span data-ttu-id="8899e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8899e-118">Remarks</span></span>

<span data-ttu-id="8899e-119">Isso é útil principalmente para passar funções a funções ou operações que esperam uma operação como entrada.</span><span class="sxs-lookup"><span data-stu-id="8899e-119">This is mainly useful for passing functions to functions or operations which expect an operation as input.</span></span>