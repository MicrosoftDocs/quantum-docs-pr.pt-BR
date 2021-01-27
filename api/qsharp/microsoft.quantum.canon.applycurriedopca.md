---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpCA
title: Operação ApplyCurriedOpCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpCA
qsharp.summary: ''
ms.openlocfilehash: acff5669c8d5d392a0032eaa49d279bff20a91f4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845064"
---
# <a name="applycurriedopca-operation"></a><span data-ttu-id="52be7-102">Operação ApplyCurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="52be7-102">ApplyCurriedOpCA operation</span></span>

<span data-ttu-id="52be7-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="52be7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="52be7-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="52be7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj)), first : 'T, second : 'U) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="52be7-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="52be7-105">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj--ctl"></a><span data-ttu-id="52be7-106">curriedOp: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="52be7-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="first--t"></a><span data-ttu-id="52be7-107">Primeiro: ' t</span><span class="sxs-lookup"><span data-stu-id="52be7-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="52be7-108">Segundo: ' U</span><span class="sxs-lookup"><span data-stu-id="52be7-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="52be7-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="52be7-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="52be7-110">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="52be7-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="52be7-111">T'</span><span class="sxs-lookup"><span data-stu-id="52be7-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="52be7-112">' U</span><span class="sxs-lookup"><span data-stu-id="52be7-112">'U</span></span>

