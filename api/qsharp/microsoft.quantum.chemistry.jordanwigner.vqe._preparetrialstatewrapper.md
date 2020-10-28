---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE._prepareTrialStateWrapper
title: _prepareTrialStateWrapper operação
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: _prepareTrialStateWrapper
qsharp.summary: Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint. EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.
ms.openlocfilehash: bfd7b9ce8e8b2c8f322d676c640f8c2488655516
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693664"
---
# <a name="_preparetrialstatewrapper-operation"></a><span data-ttu-id="eec49-102">_prepareTrialStateWrapper operação</span><span class="sxs-lookup"><span data-stu-id="eec49-102">_prepareTrialStateWrapper operation</span></span>

<span data-ttu-id="eec49-103">Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="eec49-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="eec49-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eec49-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eec49-105">Wrapper privado em volta de PrepareTrialState para torná-lo compatível com EstimateFrequencyA definindo um erro.</span><span class="sxs-lookup"><span data-stu-id="eec49-105">Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint.</span></span>
<span data-ttu-id="eec49-106">O EstimateFrequencyA tem um recurso de emulação interno ao direcionar o QuantumSimulator, que acelera sua execução.</span><span class="sxs-lookup"><span data-stu-id="eec49-106">EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.</span></span>

```qsharp
operation _prepareTrialStateWrapper (inputState : (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="eec49-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="eec49-107">Input</span></span>

### <a name="inputstate--intjordanwignerinputstate"></a><span data-ttu-id="eec49-108">inputstate: ([int](xref:microsoft.quantum.lang-ref.int),[JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])</span><span class="sxs-lookup"><span data-stu-id="eec49-108">inputState : ([Int](xref:microsoft.quantum.lang-ref.int),[JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])</span></span>

<span data-ttu-id="eec49-109">A entrada de Jordan-Wigner necessária para a execução de PrepareTrialState.</span><span class="sxs-lookup"><span data-stu-id="eec49-109">The Jordan-Wigner input required for PrepareTrialState to run.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="eec49-110">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="eec49-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="eec49-111">Um registro do qubit.</span><span class="sxs-lookup"><span data-stu-id="eec49-111">A qubit register.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eec49-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eec49-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

