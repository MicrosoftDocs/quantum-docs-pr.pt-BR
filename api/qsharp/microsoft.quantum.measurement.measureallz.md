---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Operação MeasureAllZ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: cb3c7cab33efb612bbf5da3b51d2df5d1b8ba1df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854666"
---
# <a name="measureallz-operation"></a><span data-ttu-id="72853-102">Operação MeasureAllZ</span><span class="sxs-lookup"><span data-stu-id="72853-102">MeasureAllZ operation</span></span>

<span data-ttu-id="72853-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="72853-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="72853-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="72853-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="72853-105">Mede em conjunto um registro de qubits na base do Pauli Z.</span><span class="sxs-lookup"><span data-stu-id="72853-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="72853-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="72853-106">Description</span></span>

<span data-ttu-id="72853-107">Mede um registro de qubits no $Z \otimes Z \otimes \cdots \otimes Z $, representando a paridade de todo o registro.</span><span class="sxs-lookup"><span data-stu-id="72853-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="72853-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="72853-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="72853-109">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="72853-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="72853-110">O registro a ser medido.</span><span class="sxs-lookup"><span data-stu-id="72853-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="72853-111">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="72853-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="72853-112">O resultado da medição de $Z \otimes Z \otimes \cdots \otimes Z $.</span><span class="sxs-lookup"><span data-stu-id="72853-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>