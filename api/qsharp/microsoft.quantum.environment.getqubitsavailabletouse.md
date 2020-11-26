---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Operação GetQubitsAvailableToUse
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: ce461b03a08b4c83b9de142c957ce5c590fe9659
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201403"
---
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="0cfaf-102">Operação GetQubitsAvailableToUse</span><span class="sxs-lookup"><span data-stu-id="0cfaf-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="0cfaf-103">Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="0cfaf-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="0cfaf-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="0cfaf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="0cfaf-105">Retorna o número de qubits disponíveis no momento para uso.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="0cfaf-106">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0cfaf-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0cfaf-107">O número de qubits que podem ser alocados em uma `using` instrução.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="0cfaf-108">Se o computador de destino que está sendo usado não fornecer essas informações, `-1` será retornado.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="0cfaf-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0cfaf-109">See Also</span></span>

- [<span data-ttu-id="0cfaf-110">Microsoft. Quantum. Environment. GetQubitsAvailableToBorrow</span><span class="sxs-lookup"><span data-stu-id="0cfaf-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)