---
uid: Microsoft.Quantum.Canon.CControlled
title: Função CControlled
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: a155b00806b17258b3f87629659bc7d786e4e11d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694068"
---
# <a name="ccontrolled-function"></a><span data-ttu-id="c21f5-102">Função CControlled</span><span class="sxs-lookup"><span data-stu-id="c21f5-102">CControlled function</span></span>

<span data-ttu-id="c21f5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c21f5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c21f5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c21f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c21f5-105">Dada uma operação op, retorna uma nova operação que aplica a op se um bit de controle clássico for true.</span><span class="sxs-lookup"><span data-stu-id="c21f5-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="c21f5-106">Se `false` nada acontecer.</span><span class="sxs-lookup"><span data-stu-id="c21f5-106">If `false`, nothing happens.</span></span>

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a><span data-ttu-id="c21f5-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c21f5-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="c21f5-108">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="c21f5-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c21f5-109">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="c21f5-109">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit"></a><span data-ttu-id="c21f5-110">Saída: ([bool](xref:microsoft.quantum.lang-ref.bool), ' t) = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="c21f5-110">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c21f5-111">Uma nova operação que será op se o bit de controle clássico for true.</span><span class="sxs-lookup"><span data-stu-id="c21f5-111">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c21f5-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="c21f5-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c21f5-113">T'</span><span class="sxs-lookup"><span data-stu-id="c21f5-113">'T</span></span>

<span data-ttu-id="c21f5-114">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="c21f5-114">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="c21f5-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c21f5-115">See Also</span></span>

- [<span data-ttu-id="c21f5-116">Microsoft. Quantum. Canon. CControlledC</span><span class="sxs-lookup"><span data-stu-id="c21f5-116">Microsoft.Quantum.Canon.CControlledC</span></span>](xref:Microsoft.Quantum.Canon.CControlledC)
- [<span data-ttu-id="c21f5-117">Microsoft. Quantum. Canon. CControlledA</span><span class="sxs-lookup"><span data-stu-id="c21f5-117">Microsoft.Quantum.Canon.CControlledA</span></span>](xref:Microsoft.Quantum.Canon.CControlledA)
- [<span data-ttu-id="c21f5-118">Microsoft. Quantum. Canon. CControlledCA</span><span class="sxs-lookup"><span data-stu-id="c21f5-118">Microsoft.Quantum.Canon.CControlledCA</span></span>](xref:Microsoft.Quantum.Canon.CControlledCA)