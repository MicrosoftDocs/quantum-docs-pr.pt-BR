---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedHpqTerm
title: _JWOptimizedHpqTerm operação
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedHpqTerm
qsharp.summary: Applies time-evolution by a PQ term described by a `GeneratorIndex`.
ms.openlocfilehash: 503de03a379ac0ede3754aa7a31ac2ce84e5c675
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697005"
---
# <a name="_jwoptimizedhpqterm-operation"></a><span data-ttu-id="0cb85-102">_JWOptimizedHpqTerm operação</span><span class="sxs-lookup"><span data-stu-id="0cb85-102">_JWOptimizedHpqTerm operation</span></span>

<span data-ttu-id="0cb85-103">Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="0cb85-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="0cb85-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0cb85-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0cb85-105">Aplica a evolução de tempo por um termo de PQ descrito por um `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="0cb85-105">Applies time-evolution by a PQ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimizedHpqTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="0cb85-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0cb85-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="0cb85-107">termo: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="0cb85-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="0cb85-108">`GeneratorIndex` representando um termo de PQ.</span><span class="sxs-lookup"><span data-stu-id="0cb85-108">`GeneratorIndex` representing a PQ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="0cb85-109">Etapas: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0cb85-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0cb85-110">Duração da evolução do tempo.</span><span class="sxs-lookup"><span data-stu-id="0cb85-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="0cb85-111">parityQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0cb85-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0cb85-112">Qubit que determina o sinal de tempo de evolução.</span><span class="sxs-lookup"><span data-stu-id="0cb85-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="0cb85-113">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0cb85-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0cb85-114">Qubits Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="0cb85-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0cb85-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0cb85-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

