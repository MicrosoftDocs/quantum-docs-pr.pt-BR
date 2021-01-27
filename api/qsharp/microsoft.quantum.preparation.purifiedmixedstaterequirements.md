---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: Função PurifiedMixedStateRequirements
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 6ddb48ba66eea87a07d515ff791bfb34f2d98b76
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856826"
---
# <a name="purifiedmixedstaterequirements-function"></a><span data-ttu-id="11ebe-102">Função PurifiedMixedStateRequirements</span><span class="sxs-lookup"><span data-stu-id="11ebe-102">PurifiedMixedStateRequirements function</span></span>

<span data-ttu-id="11ebe-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="11ebe-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="11ebe-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="11ebe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="11ebe-105">Retorna o número total de qubits que deve ser alocado para aplicar a operação retornada por @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="11ebe-105">Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".</span></span>

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a><span data-ttu-id="11ebe-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="11ebe-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="11ebe-107">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="11ebe-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="11ebe-108">O erro de destino $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="11ebe-108">The target error $\epsilon$.</span></span>


### <a name="ncoefficients--int"></a><span data-ttu-id="11ebe-109">nCoefficients: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="11ebe-109">nCoefficients : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="11ebe-110">O número de coeficientes a ser especificado na preparação de um estado misto.</span><span class="sxs-lookup"><span data-stu-id="11ebe-110">The number of coefficients to be specified in preparing a mixed state.</span></span>



## <a name="output--mixedstatepreparationrequirements"></a><span data-ttu-id="11ebe-111">Saída: [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="11ebe-111">Output : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>

<span data-ttu-id="11ebe-112">Uma descrição de quantas qubits são necessárias no total e para cada um dos registros de índice e lixo usados pela @"microsoft.quantum.preparation.purifiedmixedstate" função.</span><span class="sxs-lookup"><span data-stu-id="11ebe-112">A description of how many qubits are required in total, and for each of the index and garbage registers used by the @"microsoft.quantum.preparation.purifiedmixedstate" function.</span></span>

## <a name="see-also"></a><span data-ttu-id="11ebe-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="11ebe-113">See Also</span></span>

- [<span data-ttu-id="11ebe-114">Microsoft. Quantum. Preparation. PurifiedMixedState</span><span class="sxs-lookup"><span data-stu-id="11ebe-114">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)