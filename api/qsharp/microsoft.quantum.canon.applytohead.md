---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Operação ApplyToHead
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 4e627b467e9354e774c2ead8b89ddd3ff3a42ef7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841331"
---
# <a name="applytohead-operation"></a><span data-ttu-id="1d4ac-102">Operação ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="1d4ac-102">ApplyToHead operation</span></span>

<span data-ttu-id="1d4ac-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1d4ac-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1d4ac-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1d4ac-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1d4ac-105">Aplica uma operação ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="1d4ac-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="1d4ac-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d4ac-106">Description</span></span>

<span data-ttu-id="1d4ac-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="1d4ac-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="1d4ac-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d4ac-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="1d4ac-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="1d4ac-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="1d4ac-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="1d4ac-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="1d4ac-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="1d4ac-111">targets : 'T[]</span></span>

<span data-ttu-id="1d4ac-112">Uma matriz de destinos, da qual a primeira será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="1d4ac-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1d4ac-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1d4ac-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1d4ac-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="1d4ac-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1d4ac-115">T'</span><span class="sxs-lookup"><span data-stu-id="1d4ac-115">'T</span></span>

<span data-ttu-id="1d4ac-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="1d4ac-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="1d4ac-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1d4ac-117">Example</span></span>

<span data-ttu-id="1d4ac-118">Os seguintes trechos de código Q # são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="1d4ac-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToHead(H, register);
H(Head(register));
```

## <a name="see-also"></a><span data-ttu-id="1d4ac-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1d4ac-119">See Also</span></span>

- [<span data-ttu-id="1d4ac-120">Microsoft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="1d4ac-120">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="1d4ac-121">Microsoft. Quantum. Canon. ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="1d4ac-121">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="1d4ac-122">Microsoft. Quantum. Canon. ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="1d4ac-122">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)