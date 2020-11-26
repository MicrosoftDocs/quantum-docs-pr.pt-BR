---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Operação MeasureAllZ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 6c44ab6a7983697644071f0e3cf106e9825661ee
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227073"
---
# <a name="measureallz-operation"></a><span data-ttu-id="06af2-102">Operação MeasureAllZ</span><span class="sxs-lookup"><span data-stu-id="06af2-102">MeasureAllZ operation</span></span>

<span data-ttu-id="06af2-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="06af2-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="06af2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="06af2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="06af2-105">Mede em conjunto um registro de qubits na base do Pauli Z.</span><span class="sxs-lookup"><span data-stu-id="06af2-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="06af2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="06af2-106">Description</span></span>

<span data-ttu-id="06af2-107">Mede um registro de qubits no $Z \otimes Z \otimes \cdots \otimes Z $, representando a paridade de todo o registro.</span><span class="sxs-lookup"><span data-stu-id="06af2-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="06af2-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="06af2-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="06af2-109">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="06af2-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="06af2-110">O registro a ser medido.</span><span class="sxs-lookup"><span data-stu-id="06af2-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="06af2-111">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="06af2-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="06af2-112">O resultado da medição de $Z \otimes Z \otimes \cdots \otimes Z $.</span><span class="sxs-lookup"><span data-stu-id="06af2-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>