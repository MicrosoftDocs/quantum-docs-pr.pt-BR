---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Operação ApplyToTailCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 00755df80981a09ddfd8327ee9b35761d30af4f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694118"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="08277-102">Operação ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="08277-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="08277-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="08277-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="08277-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="08277-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="08277-105">Aplica uma operação ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="08277-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="08277-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="08277-106">Description</span></span>

<span data-ttu-id="08277-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="08277-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="08277-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="08277-108">Input</span></span>

### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="08277-109">op: ' t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="08277-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="08277-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="08277-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="08277-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="08277-111">targets : 'T[]</span></span>

<span data-ttu-id="08277-112">Uma matriz de destinos, da qual a última será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="08277-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="08277-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="08277-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="08277-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="08277-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="08277-115">T'</span><span class="sxs-lookup"><span data-stu-id="08277-115">'T</span></span>

<span data-ttu-id="08277-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="08277-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="08277-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="08277-117">See Also</span></span>

- [<span data-ttu-id="08277-118">Microsoft. Quantum. Canon. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="08277-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="08277-119">Microsoft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="08277-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="08277-120">Microsoft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="08277-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)