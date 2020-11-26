---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Tipo definido pelo usuário SyndromeMeasOp
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 65e47d82546b1df0beec2c00f435d3e7a28e6ae6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200247"
---
# <a name="syndromemeasop-user-defined-type"></a><span data-ttu-id="52625-102">Tipo definido pelo usuário SyndromeMeasOp</span><span class="sxs-lookup"><span data-stu-id="52625-102">SyndromeMeasOp user defined type</span></span>

<span data-ttu-id="52625-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="52625-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="52625-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="52625-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="52625-105">Representa uma operação que é usada para medir a síndrome de um bloco de código com correção de erros.</span><span class="sxs-lookup"><span data-stu-id="52625-105">Represents an operation that is used to measure the syndrome of an error-correcting code block.</span></span>

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a><span data-ttu-id="52625-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="52625-106">Remarks</span></span>

<span data-ttu-id="52625-107">A assinatura `(LogicalRegister => Syndrome)` representa uma operação que atua em conjunto no qubits em `LogicalRegister` e em algumas qubits auxiliares seguidos por uma medida do qubits auxiliar para extrair um `Syndrome` valor que representa a `Result[]` dessas medições.</span><span class="sxs-lookup"><span data-stu-id="52625-107">The signature `(LogicalRegister => Syndrome)` represents an operation that acts jointly on the qubits in `LogicalRegister` and some auxiliary qubits followed by a measurements of the auxiliary qubits to extract a `Syndrome` value representing the `Result[]` of these measurements.</span></span>

## <a name="see-also"></a><span data-ttu-id="52625-108">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="52625-108">See Also</span></span>

- [<span data-ttu-id="52625-109">Microsoft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="52625-109">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="52625-110">Microsoft. Quantum. ErrorCorrection. síndrome</span><span class="sxs-lookup"><span data-stu-id="52625-110">Microsoft.Quantum.ErrorCorrection.Syndrome</span></span>](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)