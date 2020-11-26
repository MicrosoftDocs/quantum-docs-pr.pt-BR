---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: Operação EncodeIntoBitFlipCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: b27759caba3c5dd363dbdf24d6e5de76870173cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200944"
---
# <a name="encodeintobitflipcode-operation"></a><span data-ttu-id="e786e-102">Operação EncodeIntoBitFlipCode</span><span class="sxs-lookup"><span data-stu-id="e786e-102">EncodeIntoBitFlipCode operation</span></span>

<span data-ttu-id="e786e-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="e786e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="e786e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e786e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e786e-105">Codifica no [3, 1, 3]/⟦ 3, 1, 1 ⟧ bit-flip Code.</span><span class="sxs-lookup"><span data-stu-id="e786e-105">Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="e786e-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e786e-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="e786e-107">physRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e786e-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e786e-108">Um registro de qubits físico que representa os dados a serem protegidos.</span><span class="sxs-lookup"><span data-stu-id="e786e-108">A register of physical qubits representing the data to be protected.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="e786e-109">auxQubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e786e-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e786e-110">Um registro de qubits auxiliares inicialmente no estado $ \ket {00} $ a ser usado na codificação dos dados a serem protegidos.</span><span class="sxs-lookup"><span data-stu-id="e786e-110">A register of auxiliary qubits initially in the $\ket{00}$ state to be used in encoding the data to be protected.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="e786e-111">Saída: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="e786e-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="e786e-112">O qubits físico e auxiliar usado na codificação, representado como um registro lógico.</span><span class="sxs-lookup"><span data-stu-id="e786e-112">The physical and auxiliary qubits used in encoding, represented as a logical register.</span></span>

## <a name="see-also"></a><span data-ttu-id="e786e-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e786e-113">See Also</span></span>

- [<span data-ttu-id="e786e-114">Microsoft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="e786e-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)