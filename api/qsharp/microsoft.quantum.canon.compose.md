---
uid: Microsoft.Quantum.Canon.Compose
title: Função compor
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 02cff7eef4d55d27d5d72e6219a90b7d8f5beb3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694054"
---
# <a name="compose-function"></a><span data-ttu-id="ef717-102">Função compor</span><span class="sxs-lookup"><span data-stu-id="ef717-102">Compose function</span></span>

<span data-ttu-id="ef717-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ef717-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ef717-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ef717-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ef717-105">Retorna a composição de duas funções.</span><span class="sxs-lookup"><span data-stu-id="ef717-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="ef717-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef717-106">Description</span></span>

<span data-ttu-id="ef717-107">Dadas duas funções $f $ e $g $, retorna uma nova função representando $f \circ g $.</span><span class="sxs-lookup"><span data-stu-id="ef717-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="ef717-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="ef717-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="ef717-109">externo: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="ef717-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="ef717-110">A segunda função a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ef717-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="ef717-111">interno: ' t-> ' U</span><span class="sxs-lookup"><span data-stu-id="ef717-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="ef717-112">A primeira função a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ef717-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="ef717-113">Saída: ' t-> ' V</span><span class="sxs-lookup"><span data-stu-id="ef717-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="ef717-114">Uma nova função $h $ de modo que para todas as entradas $x $, $f (g (x)) = h (x) $.</span><span class="sxs-lookup"><span data-stu-id="ef717-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ef717-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ef717-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ef717-116">T'</span><span class="sxs-lookup"><span data-stu-id="ef717-116">'T</span></span>

<span data-ttu-id="ef717-117">O tipo de entrada da primeira função a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ef717-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="ef717-118">' U</span><span class="sxs-lookup"><span data-stu-id="ef717-118">'U</span></span>

<span data-ttu-id="ef717-119">O tipo de saída da primeira função a ser aplicada e o tipo de entrada da segunda função a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ef717-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="ef717-120">' V</span><span class="sxs-lookup"><span data-stu-id="ef717-120">'V</span></span>

<span data-ttu-id="ef717-121">O tipo de saída da segunda função a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ef717-121">The output type of the second function to be applied.</span></span>