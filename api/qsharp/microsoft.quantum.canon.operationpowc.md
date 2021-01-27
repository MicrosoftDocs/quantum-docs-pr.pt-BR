---
uid: Microsoft.Quantum.Canon.OperationPowC
title: Função OperationPowC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 05b0d5b286e16c308d8c3df8fb8fa1ac8c9868ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852343"
---
# <a name="operationpowc-function"></a><span data-ttu-id="b4f78-102">Função OperationPowC</span><span class="sxs-lookup"><span data-stu-id="b4f78-102">OperationPowC function</span></span>

<span data-ttu-id="b4f78-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b4f78-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b4f78-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b4f78-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b4f78-105">Gera uma operação para uma potência.</span><span class="sxs-lookup"><span data-stu-id="b4f78-105">Raises an operation to a power.</span></span>
<span data-ttu-id="b4f78-106">O modificador `C` indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="b4f78-106">The modifier `C` indicates that the operation is controllable.</span></span>

<span data-ttu-id="b4f78-107">Ou seja, dada uma operação que representa um portão $U $, retorna uma nova operação $U ^ m $ para um Power $m $.</span><span class="sxs-lookup"><span data-stu-id="b4f78-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="b4f78-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="b4f78-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="b4f78-109">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="b4f78-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="b4f78-110">Uma operação $U $ que representa o portão a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="b4f78-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="b4f78-111">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b4f78-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b4f78-112">O número de vezes que $U $ será repetido.</span><span class="sxs-lookup"><span data-stu-id="b4f78-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="b4f78-113">Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="b4f78-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="b4f78-114">Uma nova operação representando $U ^ m $, em que $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="b4f78-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b4f78-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b4f78-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b4f78-116">T'</span><span class="sxs-lookup"><span data-stu-id="b4f78-116">'T</span></span>

<span data-ttu-id="b4f78-117">O tipo da operação a ser alimentada.</span><span class="sxs-lookup"><span data-stu-id="b4f78-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4f78-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b4f78-118">See Also</span></span>

- [<span data-ttu-id="b4f78-119">Microsoft. Quantum. Canon. OperationPow</span><span class="sxs-lookup"><span data-stu-id="b4f78-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)