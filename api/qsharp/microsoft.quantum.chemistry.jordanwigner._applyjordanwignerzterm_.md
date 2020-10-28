---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZTerm_
title: Operação _ApplyJordanWignerZTerm_
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZTerm_
qsharp.summary: Applies time-evolution by a Z term described by a `GeneratorIndex`.
ms.openlocfilehash: f42c2ba7570f32d3f26ff82dd4a0ee6f9677fa30
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693802"
---
# <a name="_applyjordanwignerzterm_-operation"></a><span data-ttu-id="fec13-102">Operação _ApplyJordanWignerZTerm_</span><span class="sxs-lookup"><span data-stu-id="fec13-102">_ApplyJordanWignerZTerm_ operation</span></span>

<span data-ttu-id="fec13-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="fec13-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="fec13-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fec13-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fec13-105">Aplica a evolução de tempo por um termo Z descrito por um `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="fec13-105">Applies time-evolution by a Z term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="fec13-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fec13-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="fec13-107">termo: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="fec13-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="fec13-108">`GeneratorIndex` representando um termo Z.</span><span class="sxs-lookup"><span data-stu-id="fec13-108">`GeneratorIndex` representing a Z term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="fec13-109">Etapas: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fec13-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fec13-110">Duração da evolução do tempo.</span><span class="sxs-lookup"><span data-stu-id="fec13-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="fec13-111">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fec13-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fec13-112">Qubits Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="fec13-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fec13-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fec13-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

