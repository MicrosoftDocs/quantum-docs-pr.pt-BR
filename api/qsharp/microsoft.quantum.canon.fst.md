---
uid: Microsoft.Quantum.Canon.Fst
title: Função FST
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 634f11881a054df7fe79d889832ea6bd80a7394f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206928"
---
# <a name="fst-function"></a><span data-ttu-id="1447d-102">Função FST</span><span class="sxs-lookup"><span data-stu-id="1447d-102">Fst function</span></span>

<span data-ttu-id="1447d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1447d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1447d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1447d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1447d-105">Dado um par, retorna seu primeiro elemento.</span><span class="sxs-lookup"><span data-stu-id="1447d-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="1447d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1447d-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="1447d-107">par: (t, ' U)</span><span class="sxs-lookup"><span data-stu-id="1447d-107">pair : ('T,'U)</span></span>

<span data-ttu-id="1447d-108">Uma tupla com dois elementos.</span><span class="sxs-lookup"><span data-stu-id="1447d-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="1447d-109">Saída: ' t</span><span class="sxs-lookup"><span data-stu-id="1447d-109">Output : 'T</span></span>

<span data-ttu-id="1447d-110">O primeiro elemento de `pair`.</span><span class="sxs-lookup"><span data-stu-id="1447d-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1447d-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="1447d-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1447d-112">T'</span><span class="sxs-lookup"><span data-stu-id="1447d-112">'T</span></span>

<span data-ttu-id="1447d-113">O tipo do primeiro membro do par.</span><span class="sxs-lookup"><span data-stu-id="1447d-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="1447d-114">' U</span><span class="sxs-lookup"><span data-stu-id="1447d-114">'U</span></span>

<span data-ttu-id="1447d-115">O tipo do segundo membro do par.</span><span class="sxs-lookup"><span data-stu-id="1447d-115">The type of the pair's second member.</span></span>