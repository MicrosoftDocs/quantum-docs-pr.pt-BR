---
uid: Microsoft.Quantum.Logical.Conditioned
title: Função condição
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: c0f55d4db95ad1f0d2b7f291cbc6ba8ae704cb81
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198479"
---
# <a name="conditioned-function"></a><span data-ttu-id="d236b-102">Função condição</span><span class="sxs-lookup"><span data-stu-id="d236b-102">Conditioned function</span></span>

<span data-ttu-id="d236b-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d236b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d236b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d236b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d236b-105">Retorna um dos dois valores, dependendo do valor de uma condição booliana.</span><span class="sxs-lookup"><span data-stu-id="d236b-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="d236b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d236b-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="d236b-107">condição: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d236b-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d236b-108">Uma condição usada para controlar qual entrada é retornada.</span><span class="sxs-lookup"><span data-stu-id="d236b-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="d236b-109">ifTrue: ' t</span><span class="sxs-lookup"><span data-stu-id="d236b-109">ifTrue : 'T</span></span>

<span data-ttu-id="d236b-110">O valor a ser retornado quando `condition` for `true` .</span><span class="sxs-lookup"><span data-stu-id="d236b-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="d236b-111">ifFalse: ' t</span><span class="sxs-lookup"><span data-stu-id="d236b-111">ifFalse : 'T</span></span>

<span data-ttu-id="d236b-112">O valor a ser retornado quando `condition` for `false` .</span><span class="sxs-lookup"><span data-stu-id="d236b-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="d236b-113">Saída: ' t</span><span class="sxs-lookup"><span data-stu-id="d236b-113">Output : 'T</span></span>

<span data-ttu-id="d236b-114">`ifTrue` Se `condition` for `true` , e `ifFalse` caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d236b-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d236b-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d236b-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d236b-116">T'</span><span class="sxs-lookup"><span data-stu-id="d236b-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="d236b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d236b-117">Remarks</span></span>

<span data-ttu-id="d236b-118">Ao contrário do `?|` operador, essa função não é de curto circuito, de modo que ambas as entradas são totalmente avaliadas.</span><span class="sxs-lookup"><span data-stu-id="d236b-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="d236b-119">Até o comportamento de curto-circuito, os seguintes são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="d236b-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```