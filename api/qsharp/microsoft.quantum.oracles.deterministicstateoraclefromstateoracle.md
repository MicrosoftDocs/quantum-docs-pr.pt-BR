---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: Função DeterministicStateOracleFromStateOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: 183b1108ead6239e26bb0b38144cb9374e7bf285
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226750"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a><span data-ttu-id="7b6dd-102">Função DeterministicStateOracleFromStateOracle</span><span class="sxs-lookup"><span data-stu-id="7b6dd-102">DeterministicStateOracleFromStateOracle function</span></span>

<span data-ttu-id="7b6dd-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="7b6dd-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7b6dd-105">Converte um Oracle do tipo `StateOracle` em `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="7b6dd-105">Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.</span></span>

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a><span data-ttu-id="7b6dd-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7b6dd-106">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="7b6dd-107">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-107">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7b6dd-108">O índice para o sinalizador qubit do `stateOracle` $A $, que age explicitamente em dois registros: o sinalizador $f $ e o sistema $s $, por exemplo $A \ket {0} \_ f\ket {\ psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-108">The index to the flag qubit of the `stateOracle` $A$, which explicitly acts on two registers: the flag $f$ and the system $s$, e.g. $A\ket{0}\_f\ket{\psi}\_s$.</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="7b6dd-109">stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="7b6dd-110">Uma preparação de estado Oracle $A $ do tipo `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="7b6dd-110">A state preparation oracle $A$ of type `StateOracle`.</span></span>



## <a name="output--deterministicstateoracle"></a><span data-ttu-id="7b6dd-111">Saída: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-111">Output : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="7b6dd-112">A mesma preparação de estado Oracle $A $, mas agora do tipo `DeterministicStateOracle` , por isso atua em um registro em que $a, s $ não é mais explicitamente separado, por exemplo,  $A \ket{0\psi} \_ {as} $.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-112">The same state preparation oracle $A$, but now of type `DeterministicStateOracle`, so it acts on a register where $a,s$ no longer explicitly separate, e.g.  $A\ket{0\psi}\_{as}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b6dd-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7b6dd-113">See Also</span></span>

- [<span data-ttu-id="7b6dd-114">Microsoft. Quantum. oracles. StateOracle</span><span class="sxs-lookup"><span data-stu-id="7b6dd-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
- [<span data-ttu-id="7b6dd-115">Microsoft. Quantum. oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="7b6dd-115">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)