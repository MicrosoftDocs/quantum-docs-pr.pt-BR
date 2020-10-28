---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Operação IterateThroughCartesianPower
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 526d28cbf3cd356b4f48eec02b3f032f70a868d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693987"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="56d17-102">Operação IterateThroughCartesianPower</span><span class="sxs-lookup"><span data-stu-id="56d17-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="56d17-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="56d17-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="56d17-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="56d17-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="56d17-105">Aplica uma operação para cada índice na potência cartesianas de um intervalo inteiro.</span><span class="sxs-lookup"><span data-stu-id="56d17-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="56d17-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="56d17-106">Description</span></span>

<span data-ttu-id="56d17-107">Aplica iterativamente uma operação para cada elemento de uma potência cartesianas do intervalo `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="56d17-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="56d17-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="56d17-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="56d17-109">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="56d17-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="56d17-110">O poder cartesiano para o qual o intervalo `0..(bound - 1)` deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="56d17-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="56d17-111">associado: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="56d17-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="56d17-112">Uma especificação do intervalo a ser iterado, dado como o comprimento do intervalo.</span><span class="sxs-lookup"><span data-stu-id="56d17-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="56d17-113">op: [int](xref:microsoft.quantum.lang-ref.int)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="56d17-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="56d17-114">Uma operação a ser chamada para cada elemento da potência cartesianas fornecida.</span><span class="sxs-lookup"><span data-stu-id="56d17-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="56d17-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="56d17-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="56d17-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="56d17-116">See Also</span></span>

- [<span data-ttu-id="56d17-117">Microsoft. Quantum. Canon. IterateThroughCartesianProduct</span><span class="sxs-lookup"><span data-stu-id="56d17-117">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)