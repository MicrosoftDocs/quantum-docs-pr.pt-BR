---
uid: Microsoft.Quantum.Canon.CurriedOp
title: Função CurriedOp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 13bc3e195d8a4ba26b726f96e4dc6b83da43c3e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694036"
---
# <a name="curriedop-function"></a><span data-ttu-id="0b6fd-102">Função CurriedOp</span><span class="sxs-lookup"><span data-stu-id="0b6fd-102">CurriedOp function</span></span>

<span data-ttu-id="0b6fd-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0b6fd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0b6fd-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0b6fd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0b6fd-105">Retorna uma versão na forma curried de uma operação em duas entradas.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-105">Returns a curried version of an operation on two inputs.</span></span>

<span data-ttu-id="0b6fd-106">Ou seja, dada uma operação com duas entradas, essa função aplica curry isomorphism $f (x, y) \equiv f (x) (y) $ para retornar uma operação de uma entrada que retorna uma operação de uma entrada.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-106">That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.</span></span>

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a><span data-ttu-id="0b6fd-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0b6fd-107">Input</span></span>

### <a name="op--tu--unit"></a><span data-ttu-id="0b6fd-108">op: (' t, ' U) = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="0b6fd-108">op : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="0b6fd-109">Uma operação cuja entrada é um par.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-109">An operation whose input is a pair.</span></span>



## <a name="output--t---u--unit"></a><span data-ttu-id="0b6fd-110">Saída: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="0b6fd-110">Output : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="0b6fd-111">Uma operação que aceita o primeiro elemento de um par e retorna uma operação que aceita como entrada o segundo elemento da entrada da operação original.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-111">An operation which accepts the first element of a pair and returns an operation which accepts as its input the second element of the original operation's input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0b6fd-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="0b6fd-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0b6fd-113">T'</span><span class="sxs-lookup"><span data-stu-id="0b6fd-113">'T</span></span>

<span data-ttu-id="0b6fd-114">O tipo do primeiro componente de uma função definida em pares.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-114">The type of the first component of a function defined on pairs.</span></span>
### <a name="u"></a><span data-ttu-id="0b6fd-115">' U</span><span class="sxs-lookup"><span data-stu-id="0b6fd-115">'U</span></span>

<span data-ttu-id="0b6fd-116">O tipo do segundo componente de uma função definida em pares.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-116">The type of the second component of a function defined on pairs.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b6fd-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b6fd-117">Remarks</span></span>

<span data-ttu-id="0b6fd-118">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="0b6fd-118">The following are equivalent:</span></span>

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```