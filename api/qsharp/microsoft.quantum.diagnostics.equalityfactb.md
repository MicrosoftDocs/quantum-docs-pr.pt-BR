---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: Função EqualityFactB
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: a87d6690e701eb1530be3134d24884a8c19357e9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201913"
---
# <a name="equalityfactb-function"></a><span data-ttu-id="438f9-102">Função EqualityFactB</span><span class="sxs-lookup"><span data-stu-id="438f9-102">EqualityFactB function</span></span>

<span data-ttu-id="438f9-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="438f9-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="438f9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="438f9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="438f9-105">Declara que uma variável bool clássica tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="438f9-105">Asserts that a classical Bool variable has the expected value.</span></span>

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="438f9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="438f9-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="438f9-107">real: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="438f9-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="438f9-108">A variável a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="438f9-108">The variable to be checked.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="438f9-109">esperado: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="438f9-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="438f9-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="438f9-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="438f9-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="438f9-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="438f9-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="438f9-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="438f9-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="438f9-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

