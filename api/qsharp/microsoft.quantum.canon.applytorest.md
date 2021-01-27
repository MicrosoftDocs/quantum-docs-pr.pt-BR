---
uid: Microsoft.Quantum.Canon.ApplyToRest
title: Operação ApplyToRest
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRest
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: f18536a056935220feedc4ea50531c5def61d650
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850505"
---
# <a name="applytorest-operation"></a><span data-ttu-id="e3c23-102">Operação ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="e3c23-102">ApplyToRest operation</span></span>

<span data-ttu-id="e3c23-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e3c23-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e3c23-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e3c23-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e3c23-105">Aplica uma operação a todos, exceto ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="e3c23-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRest<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="e3c23-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3c23-106">Description</span></span>

<span data-ttu-id="e3c23-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="e3c23-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="e3c23-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3c23-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="e3c23-109">op: ' t [] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="e3c23-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e3c23-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="e3c23-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="e3c23-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="e3c23-111">targets : 'T[]</span></span>

<span data-ttu-id="e3c23-112">Uma matriz de destinos, das quais todos, exceto o primeiro, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="e3c23-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e3c23-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e3c23-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e3c23-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e3c23-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e3c23-115">T'</span><span class="sxs-lookup"><span data-stu-id="e3c23-115">'T</span></span>

<span data-ttu-id="e3c23-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="e3c23-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="e3c23-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3c23-117">Example</span></span>

<span data-ttu-id="e3c23-118">Os seguintes trechos de código Q # são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="e3c23-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToRest(ApplyCNOTChain, register);
ApplyCNOTChain(Rest(register));
```

## <a name="see-also"></a><span data-ttu-id="e3c23-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e3c23-119">See Also</span></span>

- [<span data-ttu-id="e3c23-120">Microsoft. Quantum. Canon. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="e3c23-120">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="e3c23-121">Microsoft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="e3c23-121">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="e3c23-122">Microsoft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="e3c23-122">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)