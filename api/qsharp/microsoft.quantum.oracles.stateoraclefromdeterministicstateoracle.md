---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: Função StateOracleFromDeterministicStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: 4eed29072cab9e8c106509a6a114c8a071441079
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842496"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="d07ab-102">Função StateOracleFromDeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="d07ab-102">StateOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="d07ab-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="d07ab-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="d07ab-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d07ab-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d07ab-105">Converte um Oracle do tipo `DeterministicStateOracle` em `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="d07ab-105">Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.</span></span>

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a><span data-ttu-id="d07ab-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d07ab-106">Input</span></span>

### <a name="deterministicstateoracle--deterministicstateoracle"></a><span data-ttu-id="d07ab-107">deterministicStateOracle: [deterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="d07ab-107">deterministicStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="d07ab-108">Uma preparação de estado Oracle $A $ do tipo `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="d07ab-108">A state preparation oracle $A$ of type `DeterministicStateOracle`.</span></span>



## <a name="output--stateoracle"></a><span data-ttu-id="d07ab-109">Saída: [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="d07ab-109">Output : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="d07ab-110">A mesma preparação de estado Oracle $A $, mas agora do tipo `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="d07ab-110">The same state preparation oracle $A$, but now of type `StateOracle`.</span></span> <span data-ttu-id="d07ab-111">Observe que o índice do sinalizador `StateOracle` é uma variável fictícia e não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="d07ab-111">Note that the flag index in this `StateOracle` is a dummy variable and has no effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="d07ab-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d07ab-112">See Also</span></span>

- [<span data-ttu-id="d07ab-113">Microsoft. Quantum. oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="d07ab-113">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="d07ab-114">Microsoft. Quantum. oracles. StateOracle</span><span class="sxs-lookup"><span data-stu-id="d07ab-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)