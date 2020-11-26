---
uid: Microsoft.Quantum.Canon.OperationPowC
title: Função OperationPowC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 71f66dd0098ab58d327fc33dbe5af191df0d3dc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205721"
---
# <a name="operationpowc-function"></a><span data-ttu-id="a7d16-102">Função OperationPowC</span><span class="sxs-lookup"><span data-stu-id="a7d16-102">OperationPowC function</span></span>

<span data-ttu-id="a7d16-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a7d16-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a7d16-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a7d16-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a7d16-105">Gera uma operação para uma potência.</span><span class="sxs-lookup"><span data-stu-id="a7d16-105">Raises an operation to a power.</span></span>
<span data-ttu-id="a7d16-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="a7d16-106">The modifier `C` indicates that the operation is controllable.</span></span>

<span data-ttu-id="a7d16-107">Ou seja, dada uma operação que representa um portão $U $, retorna uma nova operação $U ^ m $ para um Power $m $.</span><span class="sxs-lookup"><span data-stu-id="a7d16-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="a7d16-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7d16-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="a7d16-109">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="a7d16-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="a7d16-110">Uma operação $U $ que representa o portão a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="a7d16-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="a7d16-111">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a7d16-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a7d16-112">O número de vezes que $U $ será repetido.</span><span class="sxs-lookup"><span data-stu-id="a7d16-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="a7d16-113">Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="a7d16-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="a7d16-114">Uma nova operação representando $U ^ m $, em que $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="a7d16-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a7d16-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a7d16-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a7d16-116">T'</span><span class="sxs-lookup"><span data-stu-id="a7d16-116">'T</span></span>

<span data-ttu-id="a7d16-117">O tipo da operação a ser alimentada.</span><span class="sxs-lookup"><span data-stu-id="a7d16-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7d16-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a7d16-118">See Also</span></span>

- [<span data-ttu-id="a7d16-119">Microsoft. Quantum. Canon. OperationPow</span><span class="sxs-lookup"><span data-stu-id="a7d16-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)