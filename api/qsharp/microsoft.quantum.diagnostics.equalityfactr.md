---
uid: Microsoft.Quantum.Diagnostics.EqualityFactR
title: Função EqualityFactR
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactR
qsharp.summary: Asserts that a classical Result variable has the expected value.
ms.openlocfilehash: 166dff211d6db9da5d39c607af1924ffd6d276dd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201760"
---
# <a name="equalityfactr-function"></a><span data-ttu-id="3c7f2-102">Função EqualityFactR</span><span class="sxs-lookup"><span data-stu-id="3c7f2-102">EqualityFactR function</span></span>

<span data-ttu-id="3c7f2-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="3c7f2-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="3c7f2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3c7f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3c7f2-105">Declara que uma variável de resultado clássico tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-105">Asserts that a classical Result variable has the expected value.</span></span>

```qsharp
function EqualityFactR (actual : Result, expected : Result, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="3c7f2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="3c7f2-106">Input</span></span>

### <a name="actual--__invalidresult__"></a><span data-ttu-id="3c7f2-107">real: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="3c7f2-107">actual : __invalid<Result>__</span></span>

<span data-ttu-id="3c7f2-108">A variável a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-108">The variable to be checked.</span></span>


### <a name="expected--__invalidresult__"></a><span data-ttu-id="3c7f2-109">esperado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="3c7f2-109">expected : __invalid<Result>__</span></span>

<span data-ttu-id="3c7f2-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="3c7f2-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="3c7f2-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="3c7f2-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3c7f2-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3c7f2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

