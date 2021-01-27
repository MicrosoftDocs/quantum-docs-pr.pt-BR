---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Operação DiscretePhaseEstimationIteration
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 03e2300dcc2d2cb42992e074833c8cd2530e898b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839969"
---
# <a name="discretephaseestimationiteration-operation"></a><span data-ttu-id="41f7f-102">Operação DiscretePhaseEstimationIteration</span><span class="sxs-lookup"><span data-stu-id="41f7f-102">DiscretePhaseEstimationIteration operation</span></span>

<span data-ttu-id="41f7f-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="41f7f-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="41f7f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="41f7f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="41f7f-105">Executa uma única iteração de um algoritmo de estimativa de fase iterativa (controlado de forma clássica) usando potências de inteiros de um Oracle unitário.</span><span class="sxs-lookup"><span data-stu-id="41f7f-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.</span></span>

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="41f7f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="41f7f-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="41f7f-107">Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="41f7f-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="41f7f-108">Operação que atua em um inteiro e um registro, de modo que $U ^ m $ seja aplicada ao registro fornecido, em que $U $ é o unitário cuja fase deve ser estimada e onde $m $ é o número inteiro de energia fornecido para o Oracle</span><span class="sxs-lookup"><span data-stu-id="41f7f-108">Operation acting on an integer and a register, such that $U^m$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $m$ is the integer power given to the oracle</span></span>


### <a name="power--int"></a><span data-ttu-id="41f7f-109">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="41f7f-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="41f7f-110">Número de vezes para aplicar o Oracle unitário fornecido.</span><span class="sxs-lookup"><span data-stu-id="41f7f-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="41f7f-111">teta: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="41f7f-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="41f7f-112">Ângulo pelo qual inverter a fase no qubit de controle antes de agir no estado de destino.</span><span class="sxs-lookup"><span data-stu-id="41f7f-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="41f7f-113">TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="41f7f-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="41f7f-114">Registro de estado acionado pelo Oracle unitário determinado.</span><span class="sxs-lookup"><span data-stu-id="41f7f-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="41f7f-115">controlQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="41f7f-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="41f7f-116">Um qubit auxiliar usado para controlar o aplicativo do Oracle fornecido.</span><span class="sxs-lookup"><span data-stu-id="41f7f-116">An auxiliary qubit used to control the application of the given oracle.</span></span>



## <a name="output--unit"></a><span data-ttu-id="41f7f-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="41f7f-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

