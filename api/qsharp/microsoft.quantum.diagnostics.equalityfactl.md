---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: Função EqualityFactL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: 5e590af581be4e41df9d2081260409c454e3be4b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693520"
---
# <a name="equalityfactl-function"></a><span data-ttu-id="7e9c0-102">Função EqualityFactL</span><span class="sxs-lookup"><span data-stu-id="7e9c0-102">EqualityFactL function</span></span>

<span data-ttu-id="7e9c0-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="7e9c0-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="7e9c0-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7e9c0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7e9c0-105">Declara que uma variável BigInt clássica tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="7e9c0-105">Asserts that a classical BigInt variable has the expected value.</span></span>

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="7e9c0-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e9c0-106">Input</span></span>

### <a name="actual--bigint"></a><span data-ttu-id="7e9c0-107">real: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="7e9c0-107">actual : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="7e9c0-108">O número a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="7e9c0-108">The number to be checked.</span></span>


### <a name="expected--bigint"></a><span data-ttu-id="7e9c0-109">esperado: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="7e9c0-109">expected : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="7e9c0-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="7e9c0-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="7e9c0-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="7e9c0-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="7e9c0-112">Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.</span><span class="sxs-lookup"><span data-stu-id="7e9c0-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7e9c0-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7e9c0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

