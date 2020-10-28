---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Operação EncodeIntoFiveQubitCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: c9df4c5c98a78cae8b3af4597020d35469454153
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693469"
---
# <a name="encodeintofivequbitcode-operation"></a><span data-ttu-id="d07ea-102">Operação EncodeIntoFiveQubitCode</span><span class="sxs-lookup"><span data-stu-id="d07ea-102">EncodeIntoFiveQubitCode operation</span></span>

<span data-ttu-id="d07ea-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="d07ea-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="d07ea-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d07ea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d07ea-105">Codifica no código Quantum ⟦ 5, 1, 3 ⟧.</span><span class="sxs-lookup"><span data-stu-id="d07ea-105">Encodes into the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="d07ea-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d07ea-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="d07ea-107">physRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d07ea-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d07ea-108">Um qubit que representa um estado não codificado.</span><span class="sxs-lookup"><span data-stu-id="d07ea-108">A qubit representing an unencoded state.</span></span> <span data-ttu-id="d07ea-109">Esta matriz `Qubit[]` tem comprimento 1.</span><span class="sxs-lookup"><span data-stu-id="d07ea-109">This array `Qubit[]` is of length 1.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="d07ea-110">auxQubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d07ea-110">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d07ea-111">Um registro de qubits auxiliares que será usado para representar o estado codificado.</span><span class="sxs-lookup"><span data-stu-id="d07ea-111">A register of auxiliary qubits that will be used to represent the encoded state.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="d07ea-112">Saída: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="d07ea-112">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="d07ea-113">Uma matriz de qubits físico do tipo `LogicalRegister` que armazena o estado codificado.</span><span class="sxs-lookup"><span data-stu-id="d07ea-113">An array of physical qubits of type `LogicalRegister` that store the encoded state.</span></span>

## <a name="see-also"></a><span data-ttu-id="d07ea-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d07ea-114">See Also</span></span>

- [<span data-ttu-id="d07ea-115">Microsoft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="d07ea-115">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)