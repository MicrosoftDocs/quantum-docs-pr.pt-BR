---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Função OracleToDiscrete
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: d26d57c587f24e7f74102c12753bcddb00fd8a9d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696915"
---
# <a name="oracletodiscrete-function"></a><span data-ttu-id="810ad-102">Função OracleToDiscrete</span><span class="sxs-lookup"><span data-stu-id="810ad-102">OracleToDiscrete function</span></span>

<span data-ttu-id="810ad-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="810ad-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="810ad-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="810ad-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="810ad-105">Dada uma operação que representa uma "caixa preta" da Oracle, retorna um Oracle de tempo discreto que representa a "caixa preta" da Oracle repetida várias vezes.</span><span class="sxs-lookup"><span data-stu-id="810ad-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="810ad-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="810ad-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit-adj--ctl"></a><span data-ttu-id="810ad-107">blackBoxOracle: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit) do ano + CTL</span><span class="sxs-lookup"><span data-stu-id="810ad-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="810ad-108">A operação a ser exponenciaçãoda.</span><span class="sxs-lookup"><span data-stu-id="810ad-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="810ad-109">Saída: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="810ad-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="810ad-110">Uma operação parcialmente aplicada sobre a "caixa preta" da Oracle que representa o tempo discreto da Oracle</span><span class="sxs-lookup"><span data-stu-id="810ad-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>