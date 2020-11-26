---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromFiveQubitCode
title: Operação DecodeFromFiveQubitCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromFiveQubitCode
qsharp.summary: Decodes the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 77c5614684f416c7d2e12914ec6246d3ef7098fb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201097"
---
# <a name="decodefromfivequbitcode-operation"></a><span data-ttu-id="2856d-102">Operação DecodeFromFiveQubitCode</span><span class="sxs-lookup"><span data-stu-id="2856d-102">DecodeFromFiveQubitCode operation</span></span>

<span data-ttu-id="2856d-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="2856d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="2856d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2856d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2856d-105">Decodifica o código Quantum ⟦ 5, 1, 3 ⟧.</span><span class="sxs-lookup"><span data-stu-id="2856d-105">Decodes the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation DecodeFromFiveQubitCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="2856d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2856d-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="2856d-107">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="2856d-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="2856d-108">Uma matriz de qubits que representa o estado lógico de código de 5 qubit codificado.</span><span class="sxs-lookup"><span data-stu-id="2856d-108">An array of qubits representing the encoded 5-qubit code logical state.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="2856d-109">Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="2856d-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="2856d-110">Uma matriz qubit de comprimento 1 que representa o estado não codificado no primeiro parâmetro, junto com qubits auxiliar no segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2856d-110">A qubit array of length 1 representing the unencoded state in the first parameter, together with auxiliary qubits in the second parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="2856d-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2856d-111">See Also</span></span>

- [<span data-ttu-id="2856d-112">Microsoft. Quantum. ErrorCorrection. FiveQubitCodeEncoder</span><span class="sxs-lookup"><span data-stu-id="2856d-112">Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder)
- [<span data-ttu-id="2856d-113">Microsoft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="2856d-113">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)