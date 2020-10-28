---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Operação GetQubitsAvailableToBorrow
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow. This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.
ms.openlocfilehash: cb56ce4aefd7a03c0f0827b8d34688ef17988f56
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693496"
---
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="42a02-102">Operação GetQubitsAvailableToBorrow</span><span class="sxs-lookup"><span data-stu-id="42a02-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="42a02-103">Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="42a02-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="42a02-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="42a02-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="42a02-105">Retorna o número de qubits disponíveis no momento para o empréstimo.</span><span class="sxs-lookup"><span data-stu-id="42a02-105">Returns the number of qubits currently available to borrow.</span></span>
<span data-ttu-id="42a02-106">Isso inclui qubits não utilizados; ou seja, isso inclui o qubits retornado por `GetQubitsAvailableToUse` .</span><span class="sxs-lookup"><span data-stu-id="42a02-106">This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="42a02-107">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="42a02-107">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="42a02-108">O número de qubits que podem ser alocados em uma `borrowing` instrução.</span><span class="sxs-lookup"><span data-stu-id="42a02-108">The number of qubits that could be allocated in a `borrowing` statement.</span></span>
<span data-ttu-id="42a02-109">Se o computador de destino que está sendo usado não fornecer essas informações, `-1` será retornado.</span><span class="sxs-lookup"><span data-stu-id="42a02-109">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="42a02-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="42a02-110">See Also</span></span>

- [<span data-ttu-id="42a02-111">Microsoft. Quantum. Environment. GetQubitsAvailableToUse</span><span class="sxs-lookup"><span data-stu-id="42a02-111">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)