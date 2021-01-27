---
uid: Microsoft.Quantum.Characterization.QuantumPhaseEstimation
title: Operação QuantumPhaseEstimation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: QuantumPhaseEstimation
qsharp.summary: Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.
ms.openlocfilehash: 4bdf3de9dab20fa97ba47f15efec4b41a10709f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839671"
---
# <a name="quantumphaseestimation-operation"></a><span data-ttu-id="33164-102">Operação QuantumPhaseEstimation</span><span class="sxs-lookup"><span data-stu-id="33164-102">QuantumPhaseEstimation operation</span></span>

<span data-ttu-id="33164-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="33164-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="33164-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="33164-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="33164-105">Executa o algoritmo de estimativa de fase Quantum para um determinado Oracle `U` e `targetState` , em seguida, lendo a fase em um registro de Quantum big-endian.</span><span class="sxs-lookup"><span data-stu-id="33164-105">Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.</span></span>

```qsharp
operation QuantumPhaseEstimation (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[], controlRegister : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="33164-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="33164-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="33164-107">Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="33164-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="33164-108">Uma operação que implementa $U ^ m $ para o número inteiro é m.</span><span class="sxs-lookup"><span data-stu-id="33164-108">An operation implementing $U^m$ for given integer powers m.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="33164-109">TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="33164-109">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="33164-110">Um registro da Quantum que representa o estado $ \ket{\phi} $ foi acionado por $U $.</span><span class="sxs-lookup"><span data-stu-id="33164-110">A quantum register representing the state $\ket{\phi}$ acted on by $U$.</span></span> <span data-ttu-id="33164-111">Se $ \ket{\phi} $ for um eigenstate de $U $, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ para $ \phi na [0, 2 \ PI) $ uma fase desconhecida.</span><span class="sxs-lookup"><span data-stu-id="33164-111">If $\ket{\phi}$ is an eigenstate of $U$, $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi \in [0, 2\pi)$ an unknown phase.</span></span>


### <a name="controlregister--bigendian"></a><span data-ttu-id="33164-112">controlRegister: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="33164-112">controlRegister : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="33164-113">Um registro inteiro de representação big endian que pode ser usado para controlar o Oracle fornecido e que conterá uma representação de $ \phi $ seguindo o aplicativo desta operação.</span><span class="sxs-lookup"><span data-stu-id="33164-113">A big-endian representation integer register that can be used to control the provided oracle, and that will contain the a representation of $\phi$ following the application of this operation.</span></span> <span data-ttu-id="33164-114">O controlRegister é considerado para iniciar no estado inicial $ \ket{00\cdots 0} $, em que o comprimento do Registro indica a precisão desejada.</span><span class="sxs-lookup"><span data-stu-id="33164-114">The controlRegister is assumed to start in the initial state $\ket{00\cdots 0}$, where the length of the register indicates the desired precision.</span></span>



## <a name="output--unit"></a><span data-ttu-id="33164-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="33164-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

