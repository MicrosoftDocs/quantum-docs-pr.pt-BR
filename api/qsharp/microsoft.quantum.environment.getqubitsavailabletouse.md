---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Operação GetQubitsAvailableToUse
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 25d43d369193fc7453fd5ce9c50769c438a69afb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693495"
---
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="af037-102">Operação GetQubitsAvailableToUse</span><span class="sxs-lookup"><span data-stu-id="af037-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="af037-103">Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="af037-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="af037-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="af037-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="af037-105">Retorna o número de qubits disponíveis no momento para uso.</span><span class="sxs-lookup"><span data-stu-id="af037-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="af037-106">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="af037-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="af037-107">O número de qubits que podem ser alocados em uma `using` instrução.</span><span class="sxs-lookup"><span data-stu-id="af037-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="af037-108">Se o computador de destino que está sendo usado não fornecer essas informações, `-1` será retornado.</span><span class="sxs-lookup"><span data-stu-id="af037-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="af037-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="af037-109">See Also</span></span>

- [<span data-ttu-id="af037-110">Microsoft. Quantum. Environment. GetQubitsAvailableToBorrow</span><span class="sxs-lookup"><span data-stu-id="af037-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)