---
uid: Microsoft.Quantum.Canon.OperationPowCA
title: Função OperationPowCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowCA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is controllable and adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 753063452616747309e3e228ce8a702f4378c61f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693937"
---
# <a name="operationpowca-function"></a><span data-ttu-id="314be-102">Função OperationPowCA</span><span class="sxs-lookup"><span data-stu-id="314be-102">OperationPowCA function</span></span>

<span data-ttu-id="314be-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="314be-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="314be-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="314be-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="314be-105">Gera uma operação para uma potência.</span><span class="sxs-lookup"><span data-stu-id="314be-105">Raises an operation to a power.</span></span>
<span data-ttu-id="314be-106">O modificador `A` indica que a operação é controlável e de adjointable.</span><span class="sxs-lookup"><span data-stu-id="314be-106">The modifier `A` indicates that the operation is controllable and adjointable.</span></span>

<span data-ttu-id="314be-107">Ou seja, dada uma operação que representa um portão $U $, retorna uma nova operação $U ^ m $ para um Power $m $.</span><span class="sxs-lookup"><span data-stu-id="314be-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowCA<'T> (op : ('T => Unit is Ctl + Adj), power : Int) : ('T => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="314be-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="314be-108">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="314be-109">op: ' t => da [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj</span><span class="sxs-lookup"><span data-stu-id="314be-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="314be-110">Uma operação $U $ que representa o portão a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="314be-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="314be-111">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="314be-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="314be-112">O número de vezes que $U $ será repetido.</span><span class="sxs-lookup"><span data-stu-id="314be-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit-ctl--adj"></a><span data-ttu-id="314be-113">Saída: t => da [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj</span><span class="sxs-lookup"><span data-stu-id="314be-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="314be-114">Uma nova operação representando $U ^ m $, em que $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="314be-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="314be-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="314be-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="314be-116">T'</span><span class="sxs-lookup"><span data-stu-id="314be-116">'T</span></span>

<span data-ttu-id="314be-117">O tipo da operação a ser alimentada.</span><span class="sxs-lookup"><span data-stu-id="314be-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="314be-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="314be-118">See Also</span></span>

- [<span data-ttu-id="314be-119">Microsoft. Quantum. Canon. OperationPow</span><span class="sxs-lookup"><span data-stu-id="314be-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)