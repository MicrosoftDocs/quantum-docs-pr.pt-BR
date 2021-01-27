---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Operação ApplyToMostA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: eb793b3d6bc1f75a14e97420d36d0aea3038e0f5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850584"
---
# <a name="applytomosta-operation"></a><span data-ttu-id="84753-102">Operação ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="84753-102">ApplyToMostA operation</span></span>

<span data-ttu-id="84753-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="84753-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="84753-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="84753-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="84753-105">Aplica uma operação a todos, exceto ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="84753-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="84753-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="84753-106">Description</span></span>

<span data-ttu-id="84753-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="84753-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="84753-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="84753-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="84753-109">op: ' t [] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="84753-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="84753-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="84753-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="84753-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="84753-111">targets : 'T[]</span></span>

<span data-ttu-id="84753-112">Uma matriz de destinos, das quais todos, exceto o último, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="84753-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="84753-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="84753-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="84753-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="84753-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="84753-115">T'</span><span class="sxs-lookup"><span data-stu-id="84753-115">'T</span></span>

<span data-ttu-id="84753-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="84753-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="84753-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="84753-117">See Also</span></span>

- [<span data-ttu-id="84753-118">Microsoft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="84753-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="84753-119">Microsoft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="84753-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="84753-120">Microsoft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="84753-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)