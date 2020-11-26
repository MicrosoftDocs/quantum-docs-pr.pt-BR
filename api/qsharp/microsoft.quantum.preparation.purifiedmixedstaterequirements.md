---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: Função PurifiedMixedStateRequirements
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 9b8861a4112c4e6c9db994339353c771a3de81a6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229980"
---
# <a name="purifiedmixedstaterequirements-function"></a><span data-ttu-id="e15ec-102">Função PurifiedMixedStateRequirements</span><span class="sxs-lookup"><span data-stu-id="e15ec-102">PurifiedMixedStateRequirements function</span></span>

<span data-ttu-id="e15ec-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="e15ec-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="e15ec-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e15ec-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e15ec-105">Retorna o número total de qubits que deve ser alocado para aplicar a operação retornada por @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="e15ec-105">Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".</span></span>

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a><span data-ttu-id="e15ec-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e15ec-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="e15ec-107">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e15ec-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e15ec-108">O erro de destino $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="e15ec-108">The target error $\epsilon$.</span></span>


### <a name="ncoefficients--int"></a><span data-ttu-id="e15ec-109">nCoefficients: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e15ec-109">nCoefficients : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e15ec-110">O número de coeficientes a ser especificado na preparação de um estado misto.</span><span class="sxs-lookup"><span data-stu-id="e15ec-110">The number of coefficients to be specified in preparing a mixed state.</span></span>



## <a name="output--mixedstatepreparationrequirements"></a><span data-ttu-id="e15ec-111">Saída: [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="e15ec-111">Output : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>

<span data-ttu-id="e15ec-112">Uma descrição de quantas qubits são necessárias no total e para cada um dos registros de índice e lixo usados pela @"microsoft.quantum.preparation.purifiedmixedstate" função.</span><span class="sxs-lookup"><span data-stu-id="e15ec-112">A description of how many qubits are required in total, and for each of the index and garbage registers used by the @"microsoft.quantum.preparation.purifiedmixedstate" function.</span></span>

## <a name="see-also"></a><span data-ttu-id="e15ec-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e15ec-113">See Also</span></span>

- [<span data-ttu-id="e15ec-114">Microsoft. Quantum. Preparation. PurifiedMixedState</span><span class="sxs-lookup"><span data-stu-id="e15ec-114">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)