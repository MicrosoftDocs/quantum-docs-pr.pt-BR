---
uid: Microsoft.Quantum.Canon.Snd
title: Função SND
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c935a2bc9e3f5ab32669feae2bfc0f2ebf57e744
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205313"
---
# <a name="snd-function"></a><span data-ttu-id="113e6-102">Função SND</span><span class="sxs-lookup"><span data-stu-id="113e6-102">Snd function</span></span>

<span data-ttu-id="113e6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="113e6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="113e6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="113e6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="113e6-105">Dado um par, retorna seu segundo elemento.</span><span class="sxs-lookup"><span data-stu-id="113e6-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="113e6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="113e6-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="113e6-107">par: (t, ' U)</span><span class="sxs-lookup"><span data-stu-id="113e6-107">pair : ('T,'U)</span></span>

<span data-ttu-id="113e6-108">Uma tupla com dois elementos.</span><span class="sxs-lookup"><span data-stu-id="113e6-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="113e6-109">Saída: ' U</span><span class="sxs-lookup"><span data-stu-id="113e6-109">Output : 'U</span></span>

<span data-ttu-id="113e6-110">O segundo elemento de `pair` .</span><span class="sxs-lookup"><span data-stu-id="113e6-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="113e6-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="113e6-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="113e6-112">T'</span><span class="sxs-lookup"><span data-stu-id="113e6-112">'T</span></span>

<span data-ttu-id="113e6-113">O tipo do primeiro membro do par.</span><span class="sxs-lookup"><span data-stu-id="113e6-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="113e6-114">' U</span><span class="sxs-lookup"><span data-stu-id="113e6-114">'U</span></span>

<span data-ttu-id="113e6-115">O tipo do segundo membro do par.</span><span class="sxs-lookup"><span data-stu-id="113e6-115">The type of the pair's second member.</span></span>