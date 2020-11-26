---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: Operação ApplyMultiplyControlledLowDepthAnd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 1aeab429bd6304c621e0d5225b43a76eab607c84
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209189"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a><span data-ttu-id="7a19a-102">Operação ApplyMultiplyControlledLowDepthAnd</span><span class="sxs-lookup"><span data-stu-id="7a19a-102">ApplyMultiplyControlledLowDepthAnd operation</span></span>

<span data-ttu-id="7a19a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7a19a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7a19a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7a19a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7a19a-105">Implementa um portão Toffoli com vários controle, supondo que o qubit de destino seja inicializado 0.</span><span class="sxs-lookup"><span data-stu-id="7a19a-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="7a19a-106">A operação de adjoin pressupõe que o qubit de destino será redefinido como 0.</span><span class="sxs-lookup"><span data-stu-id="7a19a-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>  <span data-ttu-id="7a19a-107">Requer uma profundidade de RZ de 1, enquanto o número de qubits auxiliares é exponencial no número de qubits.</span><span class="sxs-lookup"><span data-stu-id="7a19a-107">Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.</span></span>

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="7a19a-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="7a19a-108">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="7a19a-109">controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7a19a-109">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7a19a-110">Qubits de controle</span><span class="sxs-lookup"><span data-stu-id="7a19a-110">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="7a19a-111">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7a19a-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7a19a-112">Qubit de destino</span><span class="sxs-lookup"><span data-stu-id="7a19a-112">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="7a19a-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7a19a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

