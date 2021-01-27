---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: Função TargetStateReflectionOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 4169ccf3e210e27f779311553b845ea04f2c7dc6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843898"
---
# <a name="targetstatereflectionoracle-function"></a><span data-ttu-id="3735e-102">Função TargetStateReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="3735e-102">TargetStateReflectionOracle function</span></span>

<span data-ttu-id="3735e-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="3735e-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="3735e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3735e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3735e-105">Constrói um `ReflectionOracle` sobre o estado de destino exclusivamente marcado pelo sinalizador qubit.</span><span class="sxs-lookup"><span data-stu-id="3735e-105">Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.</span></span>

<span data-ttu-id="3735e-106">O estado de destino tem um único qubit definido como 1 e todos os outros 0: $ \ket {1} _F $.</span><span class="sxs-lookup"><span data-stu-id="3735e-106">The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.</span></span>

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a><span data-ttu-id="3735e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="3735e-107">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="3735e-108">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3735e-108">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3735e-109">Index para sinalizar qubit $f $ do Oracle.</span><span class="sxs-lookup"><span data-stu-id="3735e-109">Index to flag qubit $f$ of oracle.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="3735e-110">Saída: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="3735e-110">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="3735e-111">Um `ReflectionOracle` que reflete o estado marcado por $ \ket {1} _F $.</span><span class="sxs-lookup"><span data-stu-id="3735e-111">A `ReflectionOracle` that reflects about the state marked by $\ket{1}_f$.</span></span>

## <a name="see-also"></a><span data-ttu-id="3735e-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3735e-112">See Also</span></span>

- [<span data-ttu-id="3735e-113">Microsoft. Quantum. Canon. ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="3735e-113">Microsoft.Quantum.Canon.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Canon.ReflectionOracle)