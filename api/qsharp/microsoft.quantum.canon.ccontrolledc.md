---
uid: Microsoft.Quantum.Canon.CControlledC
title: Função CControlledC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledC
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: a10c8f0f835fe7cbb8f2d89d521a548169613c0a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840972"
---
# <a name="ccontrolledc-function"></a><span data-ttu-id="08bb3-102">Função CControlledC</span><span class="sxs-lookup"><span data-stu-id="08bb3-102">CControlledC function</span></span>

<span data-ttu-id="08bb3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="08bb3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="08bb3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="08bb3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="08bb3-105">Dada uma operação op, retorna uma nova operação que aplica a op se um bit de controle clássico for true.</span><span class="sxs-lookup"><span data-stu-id="08bb3-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="08bb3-106">Se `false` nada acontecer.</span><span class="sxs-lookup"><span data-stu-id="08bb3-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="08bb3-107">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="08bb3-107">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
function CControlledC<'T> (op : ('T => Unit is Ctl)) : ((Bool, 'T) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="08bb3-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="08bb3-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="08bb3-109">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="08bb3-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="08bb3-110">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="08bb3-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-ctl"></a><span data-ttu-id="08bb3-111">Saída: ([bool](xref:microsoft.quantum.lang-ref.bool), não) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL</span><span class="sxs-lookup"><span data-stu-id="08bb3-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="08bb3-112">Uma nova operação que será op se o bit de controle clássico for true.</span><span class="sxs-lookup"><span data-stu-id="08bb3-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="08bb3-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="08bb3-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="08bb3-114">T'</span><span class="sxs-lookup"><span data-stu-id="08bb3-114">'T</span></span>

<span data-ttu-id="08bb3-115">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="08bb3-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="08bb3-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="08bb3-116">See Also</span></span>

- [<span data-ttu-id="08bb3-117">Microsoft. Quantum. Canon. CControlled</span><span class="sxs-lookup"><span data-stu-id="08bb3-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)