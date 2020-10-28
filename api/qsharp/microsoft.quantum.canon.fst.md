---
uid: Microsoft.Quantum.Canon.Fst
title: Função FST
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 88ff5e29de9eeefcc1e207f277c37c63cb0faade
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694010"
---
# <a name="fst-function"></a><span data-ttu-id="89ce0-102">Função FST</span><span class="sxs-lookup"><span data-stu-id="89ce0-102">Fst function</span></span>

<span data-ttu-id="89ce0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="89ce0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="89ce0-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="89ce0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="89ce0-105">Dado um par, retorna seu primeiro elemento.</span><span class="sxs-lookup"><span data-stu-id="89ce0-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="89ce0-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="89ce0-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="89ce0-107">par: (t, ' U)</span><span class="sxs-lookup"><span data-stu-id="89ce0-107">pair : ('T,'U)</span></span>

<span data-ttu-id="89ce0-108">Uma tupla com dois elementos.</span><span class="sxs-lookup"><span data-stu-id="89ce0-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="89ce0-109">Saída: ' t</span><span class="sxs-lookup"><span data-stu-id="89ce0-109">Output : 'T</span></span>

<span data-ttu-id="89ce0-110">O primeiro elemento de `pair`.</span><span class="sxs-lookup"><span data-stu-id="89ce0-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="89ce0-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="89ce0-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="89ce0-112">T'</span><span class="sxs-lookup"><span data-stu-id="89ce0-112">'T</span></span>

<span data-ttu-id="89ce0-113">O tipo do primeiro membro do par.</span><span class="sxs-lookup"><span data-stu-id="89ce0-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="89ce0-114">' U</span><span class="sxs-lookup"><span data-stu-id="89ce0-114">'U</span></span>

<span data-ttu-id="89ce0-115">O tipo do segundo membro do par.</span><span class="sxs-lookup"><span data-stu-id="89ce0-115">The type of the pair's second member.</span></span>