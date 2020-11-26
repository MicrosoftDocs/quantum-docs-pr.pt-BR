---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: Operação ApplyToRestA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 34cb5071dd939d0831e39bb8f1670670ae1fad31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208288"
---
# <a name="applytoresta-operation"></a><span data-ttu-id="74a08-102">Operação ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="74a08-102">ApplyToRestA operation</span></span>

<span data-ttu-id="74a08-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="74a08-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="74a08-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="74a08-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="74a08-105">Aplica uma operação a todos, exceto ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="74a08-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="74a08-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="74a08-106">Description</span></span>

<span data-ttu-id="74a08-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="74a08-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="74a08-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="74a08-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="74a08-109">op: ' t [] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="74a08-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="74a08-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="74a08-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="74a08-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="74a08-111">targets : 'T[]</span></span>

<span data-ttu-id="74a08-112">Uma matriz de destinos, das quais todos, exceto o primeiro, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="74a08-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="74a08-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="74a08-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="74a08-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="74a08-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="74a08-115">T'</span><span class="sxs-lookup"><span data-stu-id="74a08-115">'T</span></span>

<span data-ttu-id="74a08-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="74a08-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="74a08-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="74a08-117">See Also</span></span>

- [<span data-ttu-id="74a08-118">Microsoft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="74a08-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="74a08-119">Microsoft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="74a08-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="74a08-120">Microsoft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="74a08-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)