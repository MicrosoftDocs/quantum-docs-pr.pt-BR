---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: Função DeterministicStateOracleFromStateOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: 539cc56e7ae4ead6654aaaae5353a771e06d2bfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696916"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a><span data-ttu-id="b71bc-102">Função DeterministicStateOracleFromStateOracle</span><span class="sxs-lookup"><span data-stu-id="b71bc-102">DeterministicStateOracleFromStateOracle function</span></span>

<span data-ttu-id="b71bc-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="b71bc-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="b71bc-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b71bc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b71bc-105">Converte um Oracle do tipo `StateOracle` em `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="b71bc-105">Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.</span></span>

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a><span data-ttu-id="b71bc-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b71bc-106">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="b71bc-107">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b71bc-107">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b71bc-108">O índice para o sinalizador qubit do `stateOracle` $A $, que age explicitamente em dois registros: o sinalizador $f $ e o sistema $s $, por exemplo $A \ket {0} \_ f\ket {\ psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="b71bc-108">The index to the flag qubit of the `stateOracle` $A$, which explicitly acts on two registers: the flag $f$ and the system $s$, e.g. $A\ket{0}\_f\ket{\psi}\_s$.</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="b71bc-109">stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="b71bc-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="b71bc-110">Uma preparação de estado Oracle $A $ do tipo `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="b71bc-110">A state preparation oracle $A$ of type `StateOracle`.</span></span>



## <a name="output--deterministicstateoracle"></a><span data-ttu-id="b71bc-111">Saída: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="b71bc-111">Output : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="b71bc-112">A mesma preparação de estado Oracle $A $, mas agora do tipo `DeterministicStateOracle` , por isso atua em um registro em que $a, s $ não é mais explicitamente separado, por exemplo,  $A \ket{0\psi} \_ {as} $.</span><span class="sxs-lookup"><span data-stu-id="b71bc-112">The same state preparation oracle $A$, but now of type `DeterministicStateOracle`, so it acts on a register where $a,s$ no longer explicitly separate, e.g.  $A\ket{0\psi}\_{as}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="b71bc-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b71bc-113">See Also</span></span>

- [<span data-ttu-id="b71bc-114">Microsoft. Quantum. oracles. StateOracle</span><span class="sxs-lookup"><span data-stu-id="b71bc-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
- [<span data-ttu-id="b71bc-115">Microsoft. Quantum. oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="b71bc-115">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)