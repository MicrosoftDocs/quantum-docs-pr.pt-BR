---
uid: Microsoft.Quantum.Math.PowCP
title: Função PowCP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowCP
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: 185d40acff6027a775130faaff64582c58384a90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194637"
---
# <a name="powcp-function"></a><span data-ttu-id="8c936-102">Função PowCP</span><span class="sxs-lookup"><span data-stu-id="8c936-102">PowCP function</span></span>

<span data-ttu-id="8c936-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="8c936-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="8c936-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8c936-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8c936-105">Retorna um número elevado a uma determinada potência.</span><span class="sxs-lookup"><span data-stu-id="8c936-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowCP (a : Microsoft.Quantum.Math.ComplexPolar, power : Microsoft.Quantum.Math.ComplexPolar) : Microsoft.Quantum.Math.ComplexPolar
```


## <a name="input"></a><span data-ttu-id="8c936-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8c936-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="8c936-107">r: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="8c936-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="8c936-108">O número $a $ que deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="8c936-108">The number $a$ that is to be raised.</span></span>


### <a name="power--complexpolar"></a><span data-ttu-id="8c936-109">energia: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="8c936-109">power : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="8c936-110">O Power $b $ para o qual $a $ deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="8c936-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--complexpolar"></a><span data-ttu-id="8c936-111">Saída: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="8c936-111">Output : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="8c936-112">O Power $a ^ b $</span><span class="sxs-lookup"><span data-stu-id="8c936-112">The power $a^b$</span></span>