---
uid: Microsoft.Quantum.Canon.CControlled
title: Função CControlled
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: f4d91471eae859b7018c9e7ea0c1c853619c484d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841002"
---
# <a name="ccontrolled-function"></a><span data-ttu-id="c1074-102">Função CControlled</span><span class="sxs-lookup"><span data-stu-id="c1074-102">CControlled function</span></span>

<span data-ttu-id="c1074-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c1074-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c1074-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c1074-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c1074-105">Dada uma operação op, retorna uma nova operação que aplica a op se um bit de controle clássico for true.</span><span class="sxs-lookup"><span data-stu-id="c1074-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="c1074-106">Se `false` nada acontecer.</span><span class="sxs-lookup"><span data-stu-id="c1074-106">If `false`, nothing happens.</span></span>

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a><span data-ttu-id="c1074-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c1074-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="c1074-108">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="c1074-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c1074-109">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="c1074-109">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit"></a><span data-ttu-id="c1074-110">Saída: ([bool](xref:microsoft.quantum.lang-ref.bool), ' t) = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="c1074-110">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c1074-111">Uma nova operação que será op se o bit de controle clássico for true.</span><span class="sxs-lookup"><span data-stu-id="c1074-111">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c1074-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="c1074-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c1074-113">T'</span><span class="sxs-lookup"><span data-stu-id="c1074-113">'T</span></span>

<span data-ttu-id="c1074-114">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="c1074-114">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1074-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c1074-115">See Also</span></span>

- [<span data-ttu-id="c1074-116">Microsoft. Quantum. Canon. CControlledC</span><span class="sxs-lookup"><span data-stu-id="c1074-116">Microsoft.Quantum.Canon.CControlledC</span></span>](xref:Microsoft.Quantum.Canon.CControlledC)
- [<span data-ttu-id="c1074-117">Microsoft. Quantum. Canon. CControlledA</span><span class="sxs-lookup"><span data-stu-id="c1074-117">Microsoft.Quantum.Canon.CControlledA</span></span>](xref:Microsoft.Quantum.Canon.CControlledA)
- [<span data-ttu-id="c1074-118">Microsoft. Quantum. Canon. CControlledCA</span><span class="sxs-lookup"><span data-stu-id="c1074-118">Microsoft.Quantum.Canon.CControlledCA</span></span>](xref:Microsoft.Quantum.Canon.CControlledCA)