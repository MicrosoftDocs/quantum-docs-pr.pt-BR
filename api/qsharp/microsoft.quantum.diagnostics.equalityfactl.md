---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: Função EqualityFactL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: b7d37b5115c51596c1b3ed93c53a29e9f36b811d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829138"
---
# <a name="equalityfactl-function"></a><span data-ttu-id="157cc-102">Função EqualityFactL</span><span class="sxs-lookup"><span data-stu-id="157cc-102">EqualityFactL function</span></span>

<span data-ttu-id="157cc-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="157cc-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="157cc-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="157cc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="157cc-105">Declara que uma variável BigInt clássica tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="157cc-105">Asserts that a classical BigInt variable has the expected value.</span></span>

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="157cc-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="157cc-106">Input</span></span>

### <a name="actual--bigint"></a><span data-ttu-id="157cc-107">real: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="157cc-107">actual : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="157cc-108">O número a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="157cc-108">The number to be checked.</span></span>


### <a name="expected--bigint"></a><span data-ttu-id="157cc-109">esperado: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="157cc-109">expected : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="157cc-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="157cc-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="157cc-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="157cc-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="157cc-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="157cc-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="157cc-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="157cc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

