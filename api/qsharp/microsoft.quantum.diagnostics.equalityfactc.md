---
uid: Microsoft.Quantum.Diagnostics.EqualityFactC
title: Função EqualityFactC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactC
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: e33d25899580a127171fb45a92d77cfdb5003a21
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201896"
---
# <a name="equalityfactc-function"></a><span data-ttu-id="da8b2-102">Função EqualityFactC</span><span class="sxs-lookup"><span data-stu-id="da8b2-102">EqualityFactC function</span></span>

<span data-ttu-id="da8b2-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="da8b2-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="da8b2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="da8b2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="da8b2-105">Declara que um número complexo tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="da8b2-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactC (actual : Microsoft.Quantum.Math.Complex, expected : Microsoft.Quantum.Math.Complex, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="da8b2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="da8b2-106">Input</span></span>

### <a name="actual--complex"></a><span data-ttu-id="da8b2-107">real: [complexo](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="da8b2-107">actual : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="da8b2-108">O valor a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="da8b2-108">The value to be checked.</span></span>


### <a name="expected--complex"></a><span data-ttu-id="da8b2-109">esperado: [complexo](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="da8b2-109">expected : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="da8b2-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="da8b2-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="da8b2-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="da8b2-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="da8b2-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="da8b2-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="da8b2-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="da8b2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

