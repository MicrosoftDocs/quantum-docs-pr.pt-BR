---
uid: Microsoft.Quantum.Diagnostics.EqualityFactC
title: Função EqualityFactC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactC
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: 4c7256f9a8c84b4e105b1cbff6b18d6dd99cc441
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693524"
---
# <a name="equalityfactc-function"></a><span data-ttu-id="47583-102">Função EqualityFactC</span><span class="sxs-lookup"><span data-stu-id="47583-102">EqualityFactC function</span></span>

<span data-ttu-id="47583-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="47583-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="47583-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="47583-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="47583-105">Declara que um número complexo tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="47583-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactC (actual : Microsoft.Quantum.Math.Complex, expected : Microsoft.Quantum.Math.Complex, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="47583-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="47583-106">Input</span></span>

### <a name="actual--complex"></a><span data-ttu-id="47583-107">real: [complexo](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="47583-107">actual : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="47583-108">O valor a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="47583-108">The value to be checked.</span></span>


### <a name="expected--complex"></a><span data-ttu-id="47583-109">esperado: [complexo](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="47583-109">expected : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="47583-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="47583-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="47583-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="47583-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="47583-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="47583-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="47583-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="47583-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
