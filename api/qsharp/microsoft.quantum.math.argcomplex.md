---
uid: Microsoft.Quantum.Math.ArgComplex
title: Função ArgComplex
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 259296f397207cde4a7d6dfe6cfb1a18e8055216
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211093"
---
# <a name="argcomplex-function"></a><span data-ttu-id="2867b-102">Função ArgComplex</span><span class="sxs-lookup"><span data-stu-id="2867b-102">ArgComplex function</span></span>

<span data-ttu-id="2867b-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2867b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2867b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2867b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2867b-105">Retorna a fase de um número complexo de tipo `Complex` .</span><span class="sxs-lookup"><span data-stu-id="2867b-105">Returns the phase of a complex number of type `Complex`.</span></span>

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="2867b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2867b-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="2867b-107">entrada: [complexo](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="2867b-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="2867b-108">Número complexo $c = x + i y $.</span><span class="sxs-lookup"><span data-stu-id="2867b-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="2867b-109">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2867b-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2867b-110">Fase $ \text{Arg} [c] = \text{ArcTan} (y, x) na (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="2867b-110">Phase $\text{Arg}[c] = \text{ArcTan}(y,x) \in (-\pi,\pi]$.</span></span>