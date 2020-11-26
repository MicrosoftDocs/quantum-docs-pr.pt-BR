---
uid: Microsoft.Quantum.Diagnostics.EqualityFactI
title: Função EqualityFactI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactI
qsharp.summary: Asserts that a classical Int variable has the expected value.
ms.openlocfilehash: 27c0642f6d89aaa715526092813240e11b9ab530
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201828"
---
# <a name="equalityfacti-function"></a><span data-ttu-id="ead38-102">Função EqualityFactI</span><span class="sxs-lookup"><span data-stu-id="ead38-102">EqualityFactI function</span></span>

<span data-ttu-id="ead38-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="ead38-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="ead38-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ead38-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ead38-105">Declara que uma variável int clássica tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="ead38-105">Asserts that a classical Int variable has the expected value.</span></span>

```qsharp
function EqualityFactI (actual : Int, expected : Int, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="ead38-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ead38-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="ead38-107">real: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ead38-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ead38-108">O número a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="ead38-108">The number to be checked.</span></span>


### <a name="expected--int"></a><span data-ttu-id="ead38-109">esperado: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ead38-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ead38-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="ead38-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="ead38-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="ead38-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="ead38-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="ead38-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ead38-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ead38-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

