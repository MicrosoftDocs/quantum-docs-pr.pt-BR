---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: Função ReflectionOracleFromDeterministicStateOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c2d37216aebcdc5243d0f1d6ec9db261cc9bd0c8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694950"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="8b701-102">Função ReflectionOracleFromDeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="8b701-102">ReflectionOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="8b701-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="8b701-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="8b701-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8b701-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8b701-105">Constrói a reflexão sobre um determinado estado de um Oracle.</span><span class="sxs-lookup"><span data-stu-id="8b701-105">Constructs reflection about a given state from an oracle.</span></span>

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a><span data-ttu-id="8b701-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b701-106">Description</span></span>

<span data-ttu-id="8b701-107">Considerando uma preparação de estado determinística Oracle representada por uma matriz unitário $O $, o resultado dessa função é um Oracle que aplica uma reflexão sobre o estado $ \ket{\psi} $ preparado pelo Oracle $O $; ou seja, o estado $ \ket{\psi} $, que $O \ket {0} = \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="8b701-107">Given a deterministic state preparation oracle represented by a unitary matrix $O$, the result of this function is an oracle that applies a reflection around the state $\ket{\psi}$ prepared by the oracle $O$; that is, the state $\ket{\psi}$ such that $O\ket{0} = \ket{\psi}$.</span></span>

## <a name="input"></a><span data-ttu-id="8b701-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b701-108">Input</span></span>

### <a name="oracle--deterministicstateoracle"></a><span data-ttu-id="8b701-109">Oracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="8b701-109">oracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="8b701-110">Um Oracle que prepara cópias do estado $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="8b701-110">An oracle that prepares copies of the state $\ket{\psi}$.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="8b701-111">Saída: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="8b701-111">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="8b701-112">Um Oracle que reflete o estado $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="8b701-112">An oracle that reflects about the state $\ket{\psi}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b701-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8b701-113">See Also</span></span>

- [<span data-ttu-id="8b701-114">Microsoft. Quantum. oracles. DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="8b701-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="8b701-115">Microsoft. Quantum. oracles. ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="8b701-115">Microsoft.Quantum.Oracles.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Oracles.ReflectionOracle)