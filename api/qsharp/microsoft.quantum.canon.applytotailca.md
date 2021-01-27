---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Operação ApplyToTailCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 4c702a9d310adae7a4ec404f3cf12893547623b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841193"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="d703a-102">Operação ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="d703a-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="d703a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d703a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d703a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d703a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d703a-105">Aplica uma operação ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="d703a-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="d703a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d703a-106">Description</span></span>

<span data-ttu-id="d703a-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="d703a-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="d703a-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="d703a-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="d703a-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="d703a-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="d703a-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="d703a-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="d703a-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="d703a-111">targets : 'T[]</span></span>

<span data-ttu-id="d703a-112">Uma matriz de destinos, da qual a última será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="d703a-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d703a-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d703a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d703a-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d703a-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d703a-115">T'</span><span class="sxs-lookup"><span data-stu-id="d703a-115">'T</span></span>

<span data-ttu-id="d703a-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="d703a-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d703a-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d703a-117">See Also</span></span>

- [<span data-ttu-id="d703a-118">Microsoft. Quantum. Canon. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="d703a-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="d703a-119">Microsoft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="d703a-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="d703a-120">Microsoft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="d703a-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)