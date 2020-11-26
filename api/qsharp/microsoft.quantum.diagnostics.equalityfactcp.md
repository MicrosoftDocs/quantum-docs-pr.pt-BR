---
uid: Microsoft.Quantum.Diagnostics.EqualityFactCP
title: Função EqualityFactCP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactCP
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: 39b55e17302f9d2e5049169e9c1a74e53a8b1115
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201845"
---
# <a name="equalityfactcp-function"></a><span data-ttu-id="bb9a0-102">Função EqualityFactCP</span><span class="sxs-lookup"><span data-stu-id="bb9a0-102">EqualityFactCP function</span></span>

<span data-ttu-id="bb9a0-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="bb9a0-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="bb9a0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bb9a0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bb9a0-105">Declara que um número complexo tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="bb9a0-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="bb9a0-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb9a0-106">Input</span></span>

### <a name="actual--complexpolar"></a><span data-ttu-id="bb9a0-107">real: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="bb9a0-107">actual : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="bb9a0-108">O valor a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="bb9a0-108">The value to be checked.</span></span>


### <a name="expected--complexpolar"></a><span data-ttu-id="bb9a0-109">esperado: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="bb9a0-109">expected : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="bb9a0-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="bb9a0-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="bb9a0-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="bb9a0-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="bb9a0-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="bb9a0-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bb9a0-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bb9a0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

