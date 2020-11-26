---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Função RMEncoding
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: a506ccb637b331a392ea75383c8bd605114af059
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202933"
---
# <a name="rmencoding-function"></a><span data-ttu-id="454b9-102">Função RMEncoding</span><span class="sxs-lookup"><span data-stu-id="454b9-102">RMEncoding function</span></span>

<span data-ttu-id="454b9-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="454b9-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="454b9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="454b9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="454b9-105">{-1,1} codificação de um valor de verdade booliano</span><span class="sxs-lookup"><span data-stu-id="454b9-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="454b9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="454b9-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="454b9-107">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="454b9-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="454b9-108">Valor booliano</span><span class="sxs-lookup"><span data-stu-id="454b9-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="454b9-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="454b9-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="454b9-110">1, se `b` for false, caso contrário-1</span><span class="sxs-lookup"><span data-stu-id="454b9-110">1, if `b` is false, otherwise -1</span></span>