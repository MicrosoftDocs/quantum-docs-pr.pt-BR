---
uid: Microsoft.Quantum.Intrinsic.Message
title: Função de mensagem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 0428a46bc639bc8a0697f5bd392f85b8b9f40ee5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693330"
---
# <a name="message-function"></a><span data-ttu-id="7de31-102">Função de mensagem</span><span class="sxs-lookup"><span data-stu-id="7de31-102">Message function</span></span>

<span data-ttu-id="7de31-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="7de31-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="7de31-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7de31-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7de31-105">Registra uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="7de31-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="7de31-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7de31-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="7de31-107">msg: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="7de31-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="7de31-108">A mensagem a ser relatada.</span><span class="sxs-lookup"><span data-stu-id="7de31-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7de31-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7de31-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7de31-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7de31-110">Remarks</span></span>

<span data-ttu-id="7de31-111">O comportamento específico dessa função é dependente de simulador, mas na maioria dos casos a mensagem fornecida será gravada no console.</span><span class="sxs-lookup"><span data-stu-id="7de31-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>