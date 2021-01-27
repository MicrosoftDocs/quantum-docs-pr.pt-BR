---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: Função EqualityFactB
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: cb1d4c471c528d2d3c08c92619fafd532a88c8f0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829215"
---
# <a name="equalityfactb-function"></a><span data-ttu-id="e10ee-102">Função EqualityFactB</span><span class="sxs-lookup"><span data-stu-id="e10ee-102">EqualityFactB function</span></span>

<span data-ttu-id="e10ee-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="e10ee-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="e10ee-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e10ee-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e10ee-105">Declara que uma variável bool clássica tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="e10ee-105">Asserts that a classical Bool variable has the expected value.</span></span>

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="e10ee-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e10ee-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="e10ee-107">real: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e10ee-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e10ee-108">A variável a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="e10ee-108">The variable to be checked.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="e10ee-109">esperado: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e10ee-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e10ee-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="e10ee-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="e10ee-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="e10ee-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="e10ee-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="e10ee-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e10ee-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e10ee-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

