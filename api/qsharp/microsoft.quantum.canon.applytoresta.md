---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: Operação ApplyToRestA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 99a18e835115491cc3451a4e3b44a6ff70e9dc6c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694138"
---
# <a name="applytoresta-operation"></a><span data-ttu-id="72724-102">Operação ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="72724-102">ApplyToRestA operation</span></span>

<span data-ttu-id="72724-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="72724-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="72724-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="72724-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="72724-105">Aplica uma operação a todos, exceto ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="72724-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="72724-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="72724-106">Description</span></span>

<span data-ttu-id="72724-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="72724-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="72724-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="72724-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="72724-109">op: ' t [] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="72724-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="72724-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="72724-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="72724-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="72724-111">targets : 'T[]</span></span>

<span data-ttu-id="72724-112">Uma matriz de destinos, das quais todos, exceto o primeiro, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="72724-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="72724-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="72724-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="72724-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="72724-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="72724-115">T'</span><span class="sxs-lookup"><span data-stu-id="72724-115">'T</span></span>

<span data-ttu-id="72724-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="72724-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="72724-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="72724-117">See Also</span></span>

- [<span data-ttu-id="72724-118">Microsoft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="72724-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="72724-119">Microsoft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="72724-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="72724-120">Microsoft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="72724-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)