---
uid: Microsoft.Quantum.Diagnostics.EqualityFactCP
title: Função EqualityFactCP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactCP
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: 1ea790debb5a9123fb8bee3a5f8a1fde0a050b37
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693522"
---
# <a name="equalityfactcp-function"></a><span data-ttu-id="d3f0c-102">Função EqualityFactCP</span><span class="sxs-lookup"><span data-stu-id="d3f0c-102">EqualityFactCP function</span></span>

<span data-ttu-id="d3f0c-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="d3f0c-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="d3f0c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d3f0c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d3f0c-105">Declara que um número complexo tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="d3f0c-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="d3f0c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3f0c-106">Input</span></span>

### <a name="actual--complexpolar"></a><span data-ttu-id="d3f0c-107">real: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="d3f0c-107">actual : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="d3f0c-108">O valor a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="d3f0c-108">The value to be checked.</span></span>


### <a name="expected--complexpolar"></a><span data-ttu-id="d3f0c-109">esperado: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="d3f0c-109">expected : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="d3f0c-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="d3f0c-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="d3f0c-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="d3f0c-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="d3f0c-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="d3f0c-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d3f0c-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d3f0c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

