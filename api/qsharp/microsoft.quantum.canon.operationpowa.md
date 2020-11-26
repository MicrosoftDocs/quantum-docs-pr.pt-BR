---
uid: Microsoft.Quantum.Canon.OperationPowA
title: Função OperationPowA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 35dc76a06fd4e8c819b785fd4c588f108c918326
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205772"
---
# <a name="operationpowa-function"></a><span data-ttu-id="63fbc-102">Função OperationPowA</span><span class="sxs-lookup"><span data-stu-id="63fbc-102">OperationPowA function</span></span>

<span data-ttu-id="63fbc-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="63fbc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="63fbc-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="63fbc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="63fbc-105">Gera uma operação para uma potência.</span><span class="sxs-lookup"><span data-stu-id="63fbc-105">Raises an operation to a power.</span></span>
<span data-ttu-id="63fbc-106">O modificador `A` indica que a operação é de adjointable.</span><span class="sxs-lookup"><span data-stu-id="63fbc-106">The modifier `A` indicates that the operation is adjointable.</span></span>

<span data-ttu-id="63fbc-107">Ou seja, dada uma operação que representa um portão $U $, retorna uma nova operação $U ^ m $ para um Power $m $.</span><span class="sxs-lookup"><span data-stu-id="63fbc-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowA<'T> (op : ('T => Unit is Adj), power : Int) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="63fbc-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="63fbc-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="63fbc-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="63fbc-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="63fbc-110">Uma operação $U $ que representa o portão a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="63fbc-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="63fbc-111">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="63fbc-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="63fbc-112">O número de vezes que $U $ será repetido.</span><span class="sxs-lookup"><span data-stu-id="63fbc-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="63fbc-113">Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="63fbc-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="63fbc-114">Uma nova operação representando $U ^ m $, em que $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="63fbc-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="63fbc-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="63fbc-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="63fbc-116">T'</span><span class="sxs-lookup"><span data-stu-id="63fbc-116">'T</span></span>

<span data-ttu-id="63fbc-117">O tipo da operação a ser alimentada.</span><span class="sxs-lookup"><span data-stu-id="63fbc-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="63fbc-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="63fbc-118">See Also</span></span>

- [<span data-ttu-id="63fbc-119">Microsoft. Quantum. Canon. OperationPow</span><span class="sxs-lookup"><span data-stu-id="63fbc-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)