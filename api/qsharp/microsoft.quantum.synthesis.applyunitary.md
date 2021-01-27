---
uid: Microsoft.Quantum.Synthesis.ApplyUnitary
title: Operação ApplyUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyUnitary
qsharp.summary: >-
  Applies gate defined by 2^n x 2^n unitary matrix.

  Fails if matrix is not unitary, or has wrong size.
ms.openlocfilehash: 58215d3b05b8c6974e979d21a13869f27b436310
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859122"
---
# <a name="applyunitary-operation"></a><span data-ttu-id="70f5d-102">Operação ApplyUnitary</span><span class="sxs-lookup"><span data-stu-id="70f5d-102">ApplyUnitary operation</span></span>

<span data-ttu-id="70f5d-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="70f5d-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="70f5d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="70f5d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="70f5d-105">Aplica o portão definido por 2 ^ n x 2 ^ n matriz unitário.</span><span class="sxs-lookup"><span data-stu-id="70f5d-105">Applies gate defined by 2^n x 2^n unitary matrix.</span></span>

<span data-ttu-id="70f5d-106">Falha se a matriz não for unitário ou tiver tamanho incorreto.</span><span class="sxs-lookup"><span data-stu-id="70f5d-106">Fails if matrix is not unitary, or has wrong size.</span></span>

```qsharp
operation ApplyUnitary (unitary : Microsoft.Quantum.Math.Complex[][], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="70f5d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="70f5d-107">Input</span></span>

### <a name="unitary--complex"></a><span data-ttu-id="70f5d-108">unitário: [complexo](xref:Microsoft.Quantum.Math.Complex)[] []</span><span class="sxs-lookup"><span data-stu-id="70f5d-108">unitary : [Complex](xref:Microsoft.Quantum.Math.Complex)[][]</span></span>

<span data-ttu-id="70f5d-109">2 ^ n x 2 ^ n matriz unitário que descreve a operação.</span><span class="sxs-lookup"><span data-stu-id="70f5d-109">2^n x 2^n unitary matrix describing the operation.</span></span>
<span data-ttu-id="70f5d-110">Se matriz não for um tamanho unitário ou não for adequado, o lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="70f5d-110">If matrix is not unitary or not of suitable size, throws an exception.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="70f5d-111">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="70f5d-111">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="70f5d-112">Qubits ao qual aplicar o registro de operação de comprimento n.</span><span class="sxs-lookup"><span data-stu-id="70f5d-112">Qubits to which apply the operation - register of length n.</span></span>



## <a name="output--unit"></a><span data-ttu-id="70f5d-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="70f5d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

