---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerPQTerm_
title: Operação _ApplyJordanWignerPQTerm_
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerPQTerm_
qsharp.summary: Applies time-evolution by a PQ term described by a `GeneratorIndex`.
ms.openlocfilehash: 8a9b41e17bcc46c5aff2b18455e1eac25620fe35
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693809"
---
# <a name="_applyjordanwignerpqterm_-operation"></a><span data-ttu-id="36906-102">Operação _ApplyJordanWignerPQTerm_</span><span class="sxs-lookup"><span data-stu-id="36906-102">_ApplyJordanWignerPQTerm_ operation</span></span>

<span data-ttu-id="36906-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="36906-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="36906-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="36906-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="36906-105">Aplica a evolução de tempo por um termo de PQ descrito por um `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="36906-105">Applies time-evolution by a PQ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerPQTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, extraParityQubits : Qubit[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="36906-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="36906-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="36906-107">termo: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="36906-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="36906-108">`GeneratorIndex` representando um termo de PQ.</span><span class="sxs-lookup"><span data-stu-id="36906-108">`GeneratorIndex` representing a PQ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="36906-109">Etapas: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="36906-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="36906-110">Duração da evolução do tempo.</span><span class="sxs-lookup"><span data-stu-id="36906-110">Duration of time-evolution.</span></span>


### <a name="extraparityqubits--qubit"></a><span data-ttu-id="36906-111">extraParityQubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="36906-111">extraParityQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="36906-112">Qubits de paridade opcionais que invertem o sinal de tempo-evolução.</span><span class="sxs-lookup"><span data-stu-id="36906-112">Optional parity qubits that flip the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="36906-113">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="36906-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="36906-114">Qubits Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="36906-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="36906-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="36906-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
