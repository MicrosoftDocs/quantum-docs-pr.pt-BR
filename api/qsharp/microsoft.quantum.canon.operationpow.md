---
uid: Microsoft.Quantum.Canon.OperationPow
title: Função OperationPow
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 9ed0d32c084f183527cac0586ad699417f51df29
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852373"
---
# <a name="operationpow-function"></a><span data-ttu-id="84e1e-102">Função OperationPow</span><span class="sxs-lookup"><span data-stu-id="84e1e-102">OperationPow function</span></span>

<span data-ttu-id="84e1e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="84e1e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="84e1e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="84e1e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="84e1e-105">Gera uma operação para uma potência.</span><span class="sxs-lookup"><span data-stu-id="84e1e-105">Raises an operation to a power.</span></span>

<span data-ttu-id="84e1e-106">Ou seja, dada uma operação que representa um portão $U $, retorna uma nova operação $U ^ m $ para um Power $m $.</span><span class="sxs-lookup"><span data-stu-id="84e1e-106">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="84e1e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="84e1e-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="84e1e-108">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="84e1e-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="84e1e-109">Uma operação $U $ que representa o portão a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="84e1e-109">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="84e1e-110">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="84e1e-110">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="84e1e-111">O número de vezes que $U $ será repetido.</span><span class="sxs-lookup"><span data-stu-id="84e1e-111">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="84e1e-112">Saída: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="84e1e-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="84e1e-113">Uma nova operação representando $U ^ m $, em que $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="84e1e-113">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="84e1e-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="84e1e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="84e1e-115">T'</span><span class="sxs-lookup"><span data-stu-id="84e1e-115">'T</span></span>

<span data-ttu-id="84e1e-116">O tipo da operação a ser alimentada.</span><span class="sxs-lookup"><span data-stu-id="84e1e-116">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="84e1e-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="84e1e-117">See Also</span></span>

- [<span data-ttu-id="84e1e-118">Microsoft. Quantum. Canon. OperationPowC</span><span class="sxs-lookup"><span data-stu-id="84e1e-118">Microsoft.Quantum.Canon.OperationPowC</span></span>](xref:Microsoft.Quantum.Canon.OperationPowC)
- [<span data-ttu-id="84e1e-119">Microsoft. Quantum. Canon. OperationPowA</span><span class="sxs-lookup"><span data-stu-id="84e1e-119">Microsoft.Quantum.Canon.OperationPowA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowA)
- [<span data-ttu-id="84e1e-120">Microsoft. Quantum. Canon. OperationPowCA</span><span class="sxs-lookup"><span data-stu-id="84e1e-120">Microsoft.Quantum.Canon.OperationPowCA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowCA)