---
uid: Microsoft.Quantum.Canon.ApplyToTailA
title: Operação ApplyToTailA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 5ca22be7a38d466f9413977de663f10606171dea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841179"
---
# <a name="applytotaila-operation"></a><span data-ttu-id="36986-102">Operação ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="36986-102">ApplyToTailA operation</span></span>

<span data-ttu-id="36986-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="36986-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="36986-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="36986-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="36986-105">Aplica uma operação ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="36986-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="36986-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="36986-106">Description</span></span>

<span data-ttu-id="36986-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="36986-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="36986-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="36986-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="36986-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="36986-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="36986-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="36986-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="36986-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="36986-111">targets : 'T[]</span></span>

<span data-ttu-id="36986-112">Uma matriz de destinos, da qual a última será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="36986-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="36986-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="36986-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="36986-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="36986-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="36986-115">T'</span><span class="sxs-lookup"><span data-stu-id="36986-115">'T</span></span>

<span data-ttu-id="36986-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="36986-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="36986-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="36986-117">See Also</span></span>

- [<span data-ttu-id="36986-118">Microsoft. Quantum. Canon. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="36986-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="36986-119">Microsoft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="36986-119">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="36986-120">Microsoft. Quantum. Canon. ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="36986-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)