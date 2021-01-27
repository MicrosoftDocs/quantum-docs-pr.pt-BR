---
uid: Microsoft.Quantum.MachineLearning.ApplySequentialClassifier
title: Operação ApplySequentialClassifier
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApplySequentialClassifier
qsharp.summary: Given the structure and parameterization of a sequential classifier, applies the classifier to a register of qubits.
ms.openlocfilehash: 8186bc57e64a52e123bef8e3556d3385c4df7034
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851449"
---
# <a name="applysequentialclassifier-operation"></a><span data-ttu-id="ceb68-102">Operação ApplySequentialClassifier</span><span class="sxs-lookup"><span data-stu-id="ceb68-102">ApplySequentialClassifier operation</span></span>

<span data-ttu-id="ceb68-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ceb68-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ceb68-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ceb68-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="ceb68-105">Considerando a estrutura e a parametrização de um classificador sequencial, o aplica o classificador a um registro de qubits.</span><span class="sxs-lookup"><span data-stu-id="ceb68-105">Given the structure and parameterization of a sequential classifier, applies the classifier to a register of qubits.</span></span>

```qsharp
operation ApplySequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ceb68-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ceb68-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="ceb68-107">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="ceb68-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>




### <a name="qubits--qubit"></a><span data-ttu-id="ceb68-108">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ceb68-108">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ceb68-109">Um registro de destino ao qual o classificador deve ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="ceb68-109">A target register to which the classifier should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ceb68-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ceb68-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

