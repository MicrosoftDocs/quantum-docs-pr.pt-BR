---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: Função EqualityFactB
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: d3163281772bda392fbdd61ad58543e22022a600
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693523"
---
# <a name="equalityfactb-function"></a><span data-ttu-id="3da31-102">Função EqualityFactB</span><span class="sxs-lookup"><span data-stu-id="3da31-102">EqualityFactB function</span></span>

<span data-ttu-id="3da31-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="3da31-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="3da31-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3da31-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3da31-105">Declara que uma variável bool clássica tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="3da31-105">Asserts that a classical Bool variable has the expected value.</span></span>

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="3da31-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="3da31-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="3da31-107">real: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3da31-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3da31-108">A variável a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="3da31-108">The variable to be checked.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="3da31-109">esperado: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3da31-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3da31-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="3da31-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="3da31-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="3da31-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="3da31-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="3da31-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3da31-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3da31-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
