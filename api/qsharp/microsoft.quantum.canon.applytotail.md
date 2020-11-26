---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Operação ApplyToTail
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 6754d41e63ea0357487fa2f62bd9209843a93347
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207965"
---
# <a name="applytotail-operation"></a><span data-ttu-id="ef173-102">Operação ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="ef173-102">ApplyToTail operation</span></span>

<span data-ttu-id="ef173-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ef173-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ef173-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ef173-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ef173-105">Aplica uma operação ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="ef173-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="ef173-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef173-106">Description</span></span>

<span data-ttu-id="ef173-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="ef173-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="ef173-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="ef173-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="ef173-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="ef173-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ef173-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ef173-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ef173-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="ef173-111">targets : 'T[]</span></span>

<span data-ttu-id="ef173-112">Uma matriz de destinos, da qual a última será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="ef173-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ef173-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ef173-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ef173-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ef173-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ef173-115">T'</span><span class="sxs-lookup"><span data-stu-id="ef173-115">'T</span></span>

<span data-ttu-id="ef173-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ef173-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef173-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ef173-117">See Also</span></span>

- [<span data-ttu-id="ef173-118">Microsoft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="ef173-118">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="ef173-119">Microsoft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="ef173-119">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="ef173-120">Microsoft. Quantum. Canon. ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="ef173-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)