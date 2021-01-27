---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: Operação ApplyToTailC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 8408dff24c5c57efbedb649ac182fac49e836a3e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850432"
---
# <a name="applytotailc-operation"></a><span data-ttu-id="2be88-102">Operação ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="2be88-102">ApplyToTailC operation</span></span>

<span data-ttu-id="2be88-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2be88-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2be88-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2be88-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2be88-105">Aplica uma operação ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="2be88-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="2be88-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2be88-106">Description</span></span>

<span data-ttu-id="2be88-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="2be88-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="2be88-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="2be88-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="2be88-109">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="2be88-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="2be88-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="2be88-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="2be88-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="2be88-111">targets : 'T[]</span></span>

<span data-ttu-id="2be88-112">Uma matriz de destinos, da qual a última será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="2be88-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2be88-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2be88-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2be88-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="2be88-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2be88-115">T'</span><span class="sxs-lookup"><span data-stu-id="2be88-115">'T</span></span>

<span data-ttu-id="2be88-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="2be88-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="2be88-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2be88-117">See Also</span></span>

- [<span data-ttu-id="2be88-118">Microsoft. Quantum. Canon. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="2be88-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="2be88-119">Microsoft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="2be88-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="2be88-120">Microsoft. Quantum. Canon. ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="2be88-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)