---
uid: Microsoft.Quantum.Logical.Conditioned
title: Função condição
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: 8aabe8b018129ddee3b934c207d0a62e59fb6f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694729"
---
# <a name="conditioned-function"></a><span data-ttu-id="20ef3-102">Função condição</span><span class="sxs-lookup"><span data-stu-id="20ef3-102">Conditioned function</span></span>

<span data-ttu-id="20ef3-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="20ef3-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="20ef3-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="20ef3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="20ef3-105">Retorna um dos dois valores, dependendo do valor de uma condição booliana.</span><span class="sxs-lookup"><span data-stu-id="20ef3-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="20ef3-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="20ef3-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="20ef3-107">condição: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="20ef3-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="20ef3-108">Uma condição usada para controlar qual entrada é retornada.</span><span class="sxs-lookup"><span data-stu-id="20ef3-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="20ef3-109">ifTrue: ' t</span><span class="sxs-lookup"><span data-stu-id="20ef3-109">ifTrue : 'T</span></span>

<span data-ttu-id="20ef3-110">O valor a ser retornado quando `condition` for `true` .</span><span class="sxs-lookup"><span data-stu-id="20ef3-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="20ef3-111">ifFalse: ' t</span><span class="sxs-lookup"><span data-stu-id="20ef3-111">ifFalse : 'T</span></span>

<span data-ttu-id="20ef3-112">O valor a ser retornado quando `condition` for `false` .</span><span class="sxs-lookup"><span data-stu-id="20ef3-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="20ef3-113">Saída: ' t</span><span class="sxs-lookup"><span data-stu-id="20ef3-113">Output : 'T</span></span>

<span data-ttu-id="20ef3-114">`ifTrue` Se `condition` for `true` , e `ifFalse` caso contrário.</span><span class="sxs-lookup"><span data-stu-id="20ef3-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="20ef3-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="20ef3-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="20ef3-116">T'</span><span class="sxs-lookup"><span data-stu-id="20ef3-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="20ef3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="20ef3-117">Remarks</span></span>

<span data-ttu-id="20ef3-118">Ao contrário do `?|` operador, essa função não é de curto circuito, de modo que ambas as entradas são totalmente avaliadas.</span><span class="sxs-lookup"><span data-stu-id="20ef3-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="20ef3-119">Até o comportamento de curto-circuito, os seguintes são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="20ef3-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```