---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Função OracleToDiscrete
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: ab59cdf0ab05092a9d4e7856b7808b13df655571
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842532"
---
# <a name="oracletodiscrete-function"></a><span data-ttu-id="0a472-102">Função OracleToDiscrete</span><span class="sxs-lookup"><span data-stu-id="0a472-102">OracleToDiscrete function</span></span>

<span data-ttu-id="0a472-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="0a472-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="0a472-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0a472-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0a472-105">Dada uma operação que representa uma "caixa preta" da Oracle, retorna um Oracle de tempo discreto que representa a "caixa preta" da Oracle repetida várias vezes.</span><span class="sxs-lookup"><span data-stu-id="0a472-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="0a472-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0a472-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a><span data-ttu-id="0a472-107">blackBoxOracle: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="0a472-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="0a472-108">A operação a ser exponenciaçãoda.</span><span class="sxs-lookup"><span data-stu-id="0a472-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="0a472-109">Saída: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="0a472-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="0a472-110">Uma operação parcialmente aplicada sobre a "caixa preta" da Oracle que representa o tempo discreto da Oracle</span><span class="sxs-lookup"><span data-stu-id="0a472-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>

## <a name="example"></a><span data-ttu-id="0a472-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0a472-111">Example</span></span>

<span data-ttu-id="0a472-112">`OracleToDiscrete(U)(3, target)` é equivalente a `U(target)` repetir três vezes.</span><span class="sxs-lookup"><span data-stu-id="0a472-112">`OracleToDiscrete(U)(3, target)` is equivalent to `U(target)` repeated three times.</span></span>