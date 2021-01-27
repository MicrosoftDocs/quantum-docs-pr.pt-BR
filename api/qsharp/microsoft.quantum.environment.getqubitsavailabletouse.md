---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Operação GetQubitsAvailableToUse
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 2ed8c3789331a15b351769be960d06f6364d8047
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827794"
---
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="668e9-102">Operação GetQubitsAvailableToUse</span><span class="sxs-lookup"><span data-stu-id="668e9-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="668e9-103">Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="668e9-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="668e9-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="668e9-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="668e9-105">Retorna o número de qubits disponíveis no momento para uso.</span><span class="sxs-lookup"><span data-stu-id="668e9-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="668e9-106">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="668e9-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="668e9-107">O número de qubits que podem ser alocados em uma `using` instrução.</span><span class="sxs-lookup"><span data-stu-id="668e9-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="668e9-108">Se o computador de destino que está sendo usado não fornecer essas informações, `-1` será retornado.</span><span class="sxs-lookup"><span data-stu-id="668e9-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="668e9-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="668e9-109">See Also</span></span>

- [<span data-ttu-id="668e9-110">Microsoft. Quantum. Environment. GetQubitsAvailableToBorrow</span><span class="sxs-lookup"><span data-stu-id="668e9-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)