---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: Operação ApplyToRestA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 69001f6c8d65806e7259f2d2f2741d48866daa84
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841257"
---
# <a name="applytoresta-operation"></a><span data-ttu-id="ce0e8-102">Operação ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="ce0e8-102">ApplyToRestA operation</span></span>

<span data-ttu-id="ce0e8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ce0e8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ce0e8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ce0e8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ce0e8-105">Aplica uma operação a todos, exceto ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="ce0e8-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="ce0e8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce0e8-106">Description</span></span>

<span data-ttu-id="ce0e8-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="ce0e8-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="ce0e8-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce0e8-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="ce0e8-109">op: ' t [] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="ce0e8-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ce0e8-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ce0e8-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ce0e8-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="ce0e8-111">targets : 'T[]</span></span>

<span data-ttu-id="ce0e8-112">Uma matriz de destinos, das quais todos, exceto o primeiro, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="ce0e8-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ce0e8-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ce0e8-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ce0e8-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ce0e8-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ce0e8-115">T'</span><span class="sxs-lookup"><span data-stu-id="ce0e8-115">'T</span></span>

<span data-ttu-id="ce0e8-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ce0e8-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce0e8-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ce0e8-117">See Also</span></span>

- [<span data-ttu-id="ce0e8-118">Microsoft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="ce0e8-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="ce0e8-119">Microsoft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="ce0e8-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="ce0e8-120">Microsoft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="ce0e8-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)