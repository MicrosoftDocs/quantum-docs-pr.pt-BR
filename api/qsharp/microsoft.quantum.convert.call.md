---
uid: Microsoft.Quantum.Convert.Call
title: Operação de chamada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 93458d08aa83ffa8b7b33de8bf51c970af291db9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850206"
---
# <a name="call-operation"></a><span data-ttu-id="9b6e3-102">Operação de chamada</span><span class="sxs-lookup"><span data-stu-id="9b6e3-102">Call operation</span></span>

<span data-ttu-id="9b6e3-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="9b6e3-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="9b6e3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b6e3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b6e3-105">Chama uma função com uma determinada entrada.</span><span class="sxs-lookup"><span data-stu-id="9b6e3-105">Calls a function with a given input.</span></span>

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a><span data-ttu-id="9b6e3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b6e3-106">Description</span></span>

<span data-ttu-id="9b6e3-107">Dada uma função e uma entrada para essa função, o chama a função e retorna sua saída.</span><span class="sxs-lookup"><span data-stu-id="9b6e3-107">Given a function and an input to that function, calls the function and returns its output.</span></span>

## <a name="input"></a><span data-ttu-id="9b6e3-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b6e3-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="9b6e3-109">FN: ' entrada-> ' saída</span><span class="sxs-lookup"><span data-stu-id="9b6e3-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="9b6e3-110">Uma função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="9b6e3-110">A function to be called.</span></span>


### <a name="input--input"></a><span data-ttu-id="9b6e3-111">entrada: ' entrada</span><span class="sxs-lookup"><span data-stu-id="9b6e3-111">input : 'Input</span></span>

<span data-ttu-id="9b6e3-112">A entrada a ser passada para a função.</span><span class="sxs-lookup"><span data-stu-id="9b6e3-112">The input to be passed to the function.</span></span>



## <a name="output--output"></a><span data-ttu-id="9b6e3-113">Saída: ' saída</span><span class="sxs-lookup"><span data-stu-id="9b6e3-113">Output : 'Output</span></span>

<span data-ttu-id="9b6e3-114">O resultado da chamada para `fn`.</span><span class="sxs-lookup"><span data-stu-id="9b6e3-114">The result of calling `fn`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9b6e3-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="9b6e3-115">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="9b6e3-116">' Entrada</span><span class="sxs-lookup"><span data-stu-id="9b6e3-116">'Input</span></span>


### <a name="output"></a><span data-ttu-id="9b6e3-117">' Saída</span><span class="sxs-lookup"><span data-stu-id="9b6e3-117">'Output</span></span>



## <a name="remarks"></a><span data-ttu-id="9b6e3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b6e3-118">Remarks</span></span>

<span data-ttu-id="9b6e3-119">Essa operação é útil principalmente para forçar a chamada de uma função em um local específico dentro de uma operação ou para chamar uma função em que uma operação é esperada.</span><span class="sxs-lookup"><span data-stu-id="9b6e3-119">This operation is mainly useful for forcing a function to be called at a specific place within an operation, or for calling a function where an operation is expected.</span></span>