---
uid: Microsoft.Quantum.Convert.Call
title: Operação de chamada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 8630f846b4b9823ce1c1dfd61dc8ca81e468517d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693631"
---
# <a name="call-operation"></a><span data-ttu-id="b6388-102">Operação de chamada</span><span class="sxs-lookup"><span data-stu-id="b6388-102">Call operation</span></span>

<span data-ttu-id="b6388-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="b6388-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="b6388-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b6388-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b6388-105">Chama uma função com uma determinada entrada.</span><span class="sxs-lookup"><span data-stu-id="b6388-105">Calls a function with a given input.</span></span>

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a><span data-ttu-id="b6388-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6388-106">Description</span></span>

<span data-ttu-id="b6388-107">Dada uma função e uma entrada para essa função, o chama a função e retorna sua saída.</span><span class="sxs-lookup"><span data-stu-id="b6388-107">Given a function and an input to that function, calls the function and returns its output.</span></span>

## <a name="input"></a><span data-ttu-id="b6388-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="b6388-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="b6388-109">FN: ' entrada-> ' saída</span><span class="sxs-lookup"><span data-stu-id="b6388-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="b6388-110">Uma função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="b6388-110">A function to be called.</span></span>


### <a name="input--input"></a><span data-ttu-id="b6388-111">entrada: ' entrada</span><span class="sxs-lookup"><span data-stu-id="b6388-111">input : 'Input</span></span>

<span data-ttu-id="b6388-112">A entrada a ser passada para a função.</span><span class="sxs-lookup"><span data-stu-id="b6388-112">The input to be passed to the function.</span></span>



## <a name="output--output"></a><span data-ttu-id="b6388-113">Saída: ' saída</span><span class="sxs-lookup"><span data-stu-id="b6388-113">Output : 'Output</span></span>

<span data-ttu-id="b6388-114">O resultado da chamada para `fn`.</span><span class="sxs-lookup"><span data-stu-id="b6388-114">The result of calling `fn`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b6388-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b6388-115">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="b6388-116">' Entrada</span><span class="sxs-lookup"><span data-stu-id="b6388-116">'Input</span></span>


### <a name="output"></a><span data-ttu-id="b6388-117">' Saída</span><span class="sxs-lookup"><span data-stu-id="b6388-117">'Output</span></span>



## <a name="remarks"></a><span data-ttu-id="b6388-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6388-118">Remarks</span></span>

<span data-ttu-id="b6388-119">Essa operação é útil principalmente para forçar a chamada de uma função em um local específico dentro de uma operação ou para chamar uma função em que uma operação é esperada.</span><span class="sxs-lookup"><span data-stu-id="b6388-119">This operation is mainly useful for forcing a function to be called at a specific place within an operation, or for calling a function where an operation is expected.</span></span>