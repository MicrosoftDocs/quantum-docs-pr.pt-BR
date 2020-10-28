---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Operação MeasureAllZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 4ac36a77b37f672859e61f3db89a43f4ca1fc93c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693280"
---
# <a name="measureallz-operation"></a><span data-ttu-id="3669d-102">Operação MeasureAllZ</span><span class="sxs-lookup"><span data-stu-id="3669d-102">MeasureAllZ operation</span></span>

<span data-ttu-id="3669d-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="3669d-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="3669d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3669d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3669d-105">Mede em conjunto um registro de qubits na base do Pauli Z.</span><span class="sxs-lookup"><span data-stu-id="3669d-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="3669d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3669d-106">Description</span></span>

<span data-ttu-id="3669d-107">Mede um registro de qubits no $Z \otimes Z \otimes \cdots \otimes Z $, representando a paridade de todo o registro.</span><span class="sxs-lookup"><span data-stu-id="3669d-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="3669d-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="3669d-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="3669d-109">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3669d-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3669d-110">O registro a ser medido.</span><span class="sxs-lookup"><span data-stu-id="3669d-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="3669d-111">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="3669d-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="3669d-112">O resultado da medição de $Z \otimes Z \otimes \cdots \otimes Z $.</span><span class="sxs-lookup"><span data-stu-id="3669d-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>