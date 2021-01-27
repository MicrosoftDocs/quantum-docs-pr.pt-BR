---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedZZTerm
title: _JWOptimizedZZTerm operação
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedZZTerm
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: e12d146c0f706e960294580ad4b26ca83711ce33
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844349"
---
# <a name="_jwoptimizedzzterm-operation"></a><span data-ttu-id="37e75-102">_JWOptimizedZZTerm operação</span><span class="sxs-lookup"><span data-stu-id="37e75-102">_JWOptimizedZZTerm operation</span></span>

<span data-ttu-id="37e75-103">Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="37e75-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="37e75-104">Pacote: [Microsoft. Quantum. Research. química](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="37e75-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="37e75-105">Aplica a evolução de tempo por um termo ZZ descrito por um `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="37e75-105">Applies time-evolution by a ZZ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimizedZZTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="37e75-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="37e75-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="37e75-107">termo: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="37e75-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="37e75-108">`GeneratorIndex` representando um termo ZZ.</span><span class="sxs-lookup"><span data-stu-id="37e75-108">`GeneratorIndex` representing a ZZ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="37e75-109">Etapas: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="37e75-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="37e75-110">Duração da evolução do tempo.</span><span class="sxs-lookup"><span data-stu-id="37e75-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="37e75-111">parityQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="37e75-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="37e75-112">Qubit que determina o sinal de tempo de evolução.</span><span class="sxs-lookup"><span data-stu-id="37e75-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="37e75-113">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="37e75-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="37e75-114">Qubits Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="37e75-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="37e75-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="37e75-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

