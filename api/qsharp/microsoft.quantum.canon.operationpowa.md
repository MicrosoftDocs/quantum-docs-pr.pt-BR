---
uid: Microsoft.Quantum.Canon.OperationPowA
title: Função OperationPowA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 67491c3302392e9793677727606df1baaf4f205a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852366"
---
# <a name="operationpowa-function"></a><span data-ttu-id="a380b-102">Função OperationPowA</span><span class="sxs-lookup"><span data-stu-id="a380b-102">OperationPowA function</span></span>

<span data-ttu-id="a380b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a380b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a380b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a380b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a380b-105">Gera uma operação para uma potência.</span><span class="sxs-lookup"><span data-stu-id="a380b-105">Raises an operation to a power.</span></span>
<span data-ttu-id="a380b-106">O modificador `A` indica que a operação é de adjointable.</span><span class="sxs-lookup"><span data-stu-id="a380b-106">The modifier `A` indicates that the operation is adjointable.</span></span>

<span data-ttu-id="a380b-107">Ou seja, dada uma operação que representa um portão $U $, retorna uma nova operação $U ^ m $ para um Power $m $.</span><span class="sxs-lookup"><span data-stu-id="a380b-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowA<'T> (op : ('T => Unit is Adj), power : Int) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="a380b-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a380b-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="a380b-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="a380b-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="a380b-110">Uma operação $U $ que representa o portão a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="a380b-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="a380b-111">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a380b-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a380b-112">O número de vezes que $U $ será repetido.</span><span class="sxs-lookup"><span data-stu-id="a380b-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="a380b-113">Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="a380b-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="a380b-114">Uma nova operação representando $U ^ m $, em que $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="a380b-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a380b-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a380b-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a380b-116">T'</span><span class="sxs-lookup"><span data-stu-id="a380b-116">'T</span></span>

<span data-ttu-id="a380b-117">O tipo da operação a ser alimentada.</span><span class="sxs-lookup"><span data-stu-id="a380b-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="a380b-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a380b-118">See Also</span></span>

- [<span data-ttu-id="a380b-119">Microsoft. Quantum. Canon. OperationPow</span><span class="sxs-lookup"><span data-stu-id="a380b-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)