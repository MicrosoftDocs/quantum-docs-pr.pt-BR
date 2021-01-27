---
uid: Microsoft.Quantum.Diagnostics.DumpReferenceAndTarget
title: Operação DumpReferenceAndTarget
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpReferenceAndTarget
qsharp.summary: Uses DumpRegister to provide diagnostics on the state of a reference and target register. Written as separate operation to allow overriding and interpreting as separate registers, rather than as a single combined register.
ms.openlocfilehash: 7f66af8a1f6f9ab83740fbf5dcfaf55776d74eb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853404"
---
# <a name="dumpreferenceandtarget-operation"></a><span data-ttu-id="a8bce-102">Operação DumpReferenceAndTarget</span><span class="sxs-lookup"><span data-stu-id="a8bce-102">DumpReferenceAndTarget operation</span></span>

<span data-ttu-id="a8bce-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="a8bce-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="a8bce-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a8bce-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a8bce-105">Usa DumpRegister para fornecer diagnósticos sobre o estado de uma referência e um registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a8bce-105">Uses DumpRegister to provide diagnostics on the state of a reference and target register.</span></span> <span data-ttu-id="a8bce-106">Escrito como uma operação separada para permitir a substituição e a interpretação de registros separados, em vez de um único registro combinado.</span><span class="sxs-lookup"><span data-stu-id="a8bce-106">Written as separate operation to allow overriding and interpreting as separate registers, rather than as a single combined register.</span></span>

```qsharp
operation DumpReferenceAndTarget (reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="a8bce-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a8bce-107">Input</span></span>

### <a name="reference--qubit"></a><span data-ttu-id="a8bce-108">referência: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a8bce-108">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="a8bce-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a8bce-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="a8bce-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a8bce-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

