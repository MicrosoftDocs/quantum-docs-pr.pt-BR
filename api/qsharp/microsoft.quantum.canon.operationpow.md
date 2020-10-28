---
uid: Microsoft.Quantum.Canon.OperationPow
title: Função OperationPow
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 5cf9017175f44a8a0b8f865624a6c312d25aded1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693951"
---
# <a name="operationpow-function"></a><span data-ttu-id="84d10-102">Função OperationPow</span><span class="sxs-lookup"><span data-stu-id="84d10-102">OperationPow function</span></span>

<span data-ttu-id="84d10-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="84d10-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="84d10-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="84d10-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="84d10-105">Gera uma operação para uma potência.</span><span class="sxs-lookup"><span data-stu-id="84d10-105">Raises an operation to a power.</span></span>

<span data-ttu-id="84d10-106">Ou seja, dada uma operação que representa um portão $U $, retorna uma nova operação $U ^ m $ para um Power $m $.</span><span class="sxs-lookup"><span data-stu-id="84d10-106">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="84d10-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="84d10-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="84d10-108">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="84d10-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="84d10-109">Uma operação $U $ que representa o portão a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="84d10-109">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="84d10-110">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="84d10-110">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="84d10-111">O número de vezes que $U $ será repetido.</span><span class="sxs-lookup"><span data-stu-id="84d10-111">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="84d10-112">Saída: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="84d10-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="84d10-113">Uma nova operação representando $U ^ m $, em que $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="84d10-113">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="84d10-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="84d10-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="84d10-115">T'</span><span class="sxs-lookup"><span data-stu-id="84d10-115">'T</span></span>

<span data-ttu-id="84d10-116">O tipo da operação a ser alimentada.</span><span class="sxs-lookup"><span data-stu-id="84d10-116">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="84d10-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="84d10-117">See Also</span></span>

- [<span data-ttu-id="84d10-118">Microsoft. Quantum. Canon. OperationPowC</span><span class="sxs-lookup"><span data-stu-id="84d10-118">Microsoft.Quantum.Canon.OperationPowC</span></span>](xref:Microsoft.Quantum.Canon.OperationPowC)
- [<span data-ttu-id="84d10-119">Microsoft. Quantum. Canon. OperationPowA</span><span class="sxs-lookup"><span data-stu-id="84d10-119">Microsoft.Quantum.Canon.OperationPowA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowA)
- [<span data-ttu-id="84d10-120">Microsoft. Quantum. Canon. OperationPowCA</span><span class="sxs-lookup"><span data-stu-id="84d10-120">Microsoft.Quantum.Canon.OperationPowCA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowCA)