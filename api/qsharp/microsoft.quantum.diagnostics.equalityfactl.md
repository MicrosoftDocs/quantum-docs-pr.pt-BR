---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: Função EqualityFactL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: 2aaabf39d6ce49952466a877685776490ef438ad
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201794"
---
# <a name="equalityfactl-function"></a><span data-ttu-id="18a93-102">Função EqualityFactL</span><span class="sxs-lookup"><span data-stu-id="18a93-102">EqualityFactL function</span></span>

<span data-ttu-id="18a93-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="18a93-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="18a93-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="18a93-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="18a93-105">Declara que uma variável BigInt clássica tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="18a93-105">Asserts that a classical BigInt variable has the expected value.</span></span>

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="18a93-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="18a93-106">Input</span></span>

### <a name="actual--bigint"></a><span data-ttu-id="18a93-107">real: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="18a93-107">actual : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="18a93-108">O número a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="18a93-108">The number to be checked.</span></span>


### <a name="expected--bigint"></a><span data-ttu-id="18a93-109">esperado: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="18a93-109">expected : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="18a93-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="18a93-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="18a93-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="18a93-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="18a93-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="18a93-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="18a93-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="18a93-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

