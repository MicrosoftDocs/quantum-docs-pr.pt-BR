---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Operação PrepareIdentity
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: 6e0a43e61e3c49edef94db63f07ed29132d84c83
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210430"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="8d762-102">Operação PrepareIdentity</span><span class="sxs-lookup"><span data-stu-id="8d762-102">PrepareIdentity operation</span></span>

<span data-ttu-id="8d762-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="8d762-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="8d762-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8d762-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8d762-105">Dado um registro, prepara esse registro no estado de forma máxima mista.</span><span class="sxs-lookup"><span data-stu-id="8d762-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="8d762-106">O registro está preparado no estado $ \boldone/2 ^ N $ aplicando o canal de despolarização completa a cada qubit, em que $N $ é o comprimento do registro.</span><span class="sxs-lookup"><span data-stu-id="8d762-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="8d762-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d762-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="8d762-108">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8d762-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8d762-109">Um registro cujo estado deve ser depolarizado da maneira descrita acima.</span><span class="sxs-lookup"><span data-stu-id="8d762-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8d762-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8d762-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="8d762-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8d762-111">See Also</span></span>

- [<span data-ttu-id="8d762-112">Microsoft. Quantum. Preparation. PrepareSingleQubitIdentity</span><span class="sxs-lookup"><span data-stu-id="8d762-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)