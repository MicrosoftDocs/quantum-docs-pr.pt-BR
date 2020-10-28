---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpC
title: Operação ApplyCurriedOpC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpC
qsharp.summary: ''
ms.openlocfilehash: 1a00fe91889e3100e4d3272d258877b4ec88618f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694318"
---
# <a name="applycurriedopc-operation"></a><span data-ttu-id="bfe42-102">Operação ApplyCurriedOpC</span><span class="sxs-lookup"><span data-stu-id="bfe42-102">ApplyCurriedOpC operation</span></span>

<span data-ttu-id="bfe42-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bfe42-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bfe42-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bfe42-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyCurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl)), first : 'T, second : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="bfe42-105">Entrada</span><span class="sxs-lookup"><span data-stu-id="bfe42-105">Input</span></span>

### <a name="curriedop--t---u--unit-ctl"></a><span data-ttu-id="bfe42-106">curriedOp: t-> ' U = CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="bfe42-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="first--t"></a><span data-ttu-id="bfe42-107">Primeiro: ' t</span><span class="sxs-lookup"><span data-stu-id="bfe42-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="bfe42-108">Segundo: ' U</span><span class="sxs-lookup"><span data-stu-id="bfe42-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="bfe42-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bfe42-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bfe42-110">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="bfe42-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bfe42-111">T'</span><span class="sxs-lookup"><span data-stu-id="bfe42-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="bfe42-112">' U</span><span class="sxs-lookup"><span data-stu-id="bfe42-112">'U</span></span>

