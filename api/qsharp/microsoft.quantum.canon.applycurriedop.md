---
uid: Microsoft.Quantum.Canon.ApplyCurriedOp
title: Operação ApplyCurriedOp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOp
qsharp.summary: ''
ms.openlocfilehash: 22e2ace51175ed9df1c70bf75ce2b497f8449020
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694321"
---
# <a name="applycurriedop-operation"></a><span data-ttu-id="7c517-102">Operação ApplyCurriedOp</span><span class="sxs-lookup"><span data-stu-id="7c517-102">ApplyCurriedOp operation</span></span>

<span data-ttu-id="7c517-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7c517-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7c517-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7c517-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyCurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit)), first : 'T, second : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="7c517-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c517-105">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="7c517-106">curriedOp: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="7c517-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="first--t"></a><span data-ttu-id="7c517-107">Primeiro: ' t</span><span class="sxs-lookup"><span data-stu-id="7c517-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="7c517-108">Segundo: ' U</span><span class="sxs-lookup"><span data-stu-id="7c517-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="7c517-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7c517-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7c517-110">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="7c517-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7c517-111">T'</span><span class="sxs-lookup"><span data-stu-id="7c517-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="7c517-112">' U</span><span class="sxs-lookup"><span data-stu-id="7c517-112">'U</span></span>

