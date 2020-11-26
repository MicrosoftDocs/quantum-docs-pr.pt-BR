---
uid: Microsoft.Quantum.Intrinsic.Message
title: Função de mensagem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 4eb55dd4fd8d78e4b5a9bb289dacfbdb3aa4beb8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96199005"
---
# <a name="message-function"></a><span data-ttu-id="17d39-102">Função de mensagem</span><span class="sxs-lookup"><span data-stu-id="17d39-102">Message function</span></span>

<span data-ttu-id="17d39-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="17d39-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="17d39-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="17d39-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="17d39-105">Registra uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="17d39-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="17d39-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="17d39-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="17d39-107">msg: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="17d39-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="17d39-108">A mensagem a ser relatada.</span><span class="sxs-lookup"><span data-stu-id="17d39-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="17d39-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="17d39-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="17d39-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="17d39-110">Remarks</span></span>

<span data-ttu-id="17d39-111">O comportamento específico dessa função é dependente de simulador, mas na maioria dos casos a mensagem fornecida será gravada no console.</span><span class="sxs-lookup"><span data-stu-id="17d39-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>