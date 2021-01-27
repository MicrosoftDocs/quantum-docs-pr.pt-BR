---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Operação ApplyToTail
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 077e6dedee68b0bd05a668387b22f8bec87a4041
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850447"
---
# <a name="applytotail-operation"></a><span data-ttu-id="edb08-102">Operação ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="edb08-102">ApplyToTail operation</span></span>

<span data-ttu-id="edb08-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="edb08-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="edb08-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="edb08-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="edb08-105">Aplica uma operação ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="edb08-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="edb08-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="edb08-106">Description</span></span>

<span data-ttu-id="edb08-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="edb08-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="edb08-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="edb08-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="edb08-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="edb08-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="edb08-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="edb08-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="edb08-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="edb08-111">targets : 'T[]</span></span>

<span data-ttu-id="edb08-112">Uma matriz de destinos, da qual a última será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="edb08-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="edb08-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="edb08-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="edb08-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="edb08-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="edb08-115">T'</span><span class="sxs-lookup"><span data-stu-id="edb08-115">'T</span></span>

<span data-ttu-id="edb08-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="edb08-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="edb08-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="edb08-117">Example</span></span>

<span data-ttu-id="edb08-118">Os seguintes trechos de código Q # são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="edb08-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToTail(H, register);
H(Tail(register));
```

## <a name="see-also"></a><span data-ttu-id="edb08-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="edb08-119">See Also</span></span>

- [<span data-ttu-id="edb08-120">Microsoft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="edb08-120">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="edb08-121">Microsoft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="edb08-121">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="edb08-122">Microsoft. Quantum. Canon. ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="edb08-122">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)