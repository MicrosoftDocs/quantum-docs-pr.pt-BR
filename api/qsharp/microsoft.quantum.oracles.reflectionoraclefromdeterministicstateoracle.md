---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: Função ReflectionOracleFromDeterministicStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c260bdbcdb2ce53ad602bf84e0d31ef4fec24a79
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842520"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="e20c8-102">Função ReflectionOracleFromDeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="e20c8-102">ReflectionOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="e20c8-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="e20c8-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="e20c8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e20c8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e20c8-105">Constrói a reflexão sobre um determinado estado de um Oracle.</span><span class="sxs-lookup"><span data-stu-id="e20c8-105">Constructs reflection about a given state from an oracle.</span></span>

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a><span data-ttu-id="e20c8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e20c8-106">Description</span></span>

<span data-ttu-id="e20c8-107">Considerando uma preparação de estado determinística Oracle representada por uma matriz unitário $O $, o resultado dessa função é um Oracle que aplica uma reflexão sobre o estado $ \ket{\psi} $ preparado pelo Oracle $O $; ou seja, o estado $ \ket{\psi} $, que $O \ket {0} = \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="e20c8-107">Given a deterministic state preparation oracle represented by a unitary matrix $O$, the result of this function is an oracle that applies a reflection around the state $\ket{\psi}$ prepared by the oracle $O$; that is, the state $\ket{\psi}$ such that $O\ket{0} = \ket{\psi}$.</span></span>

## <a name="input"></a><span data-ttu-id="e20c8-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="e20c8-108">Input</span></span>

### <a name="oracle--deterministicstateoracle"></a><span data-ttu-id="e20c8-109">Oracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="e20c8-109">oracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="e20c8-110">Um Oracle que prepara cópias do estado $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="e20c8-110">An oracle that prepares copies of the state $\ket{\psi}$.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="e20c8-111">Saída: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="e20c8-111">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="e20c8-112">Um Oracle que reflete o estado $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="e20c8-112">An oracle that reflects about the state $\ket{\psi}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="e20c8-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e20c8-113">See Also</span></span>

- [<span data-ttu-id="e20c8-114">Microsoft. Quantum. oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="e20c8-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="e20c8-115">Microsoft. Quantum. oracles. ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="e20c8-115">Microsoft.Quantum.Oracles.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Oracles.ReflectionOracle)