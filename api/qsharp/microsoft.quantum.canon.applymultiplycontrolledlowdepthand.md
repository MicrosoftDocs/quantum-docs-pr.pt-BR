---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: Operação ApplyMultiplyControlledLowDepthAnd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 6900f9b0f014fba28ae73a70f180f3e4696900cd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694262"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a><span data-ttu-id="d1d15-102">Operação ApplyMultiplyControlledLowDepthAnd</span><span class="sxs-lookup"><span data-stu-id="d1d15-102">ApplyMultiplyControlledLowDepthAnd operation</span></span>

<span data-ttu-id="d1d15-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d1d15-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d1d15-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d1d15-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d1d15-105">Implementa um portão Toffoli com vários controle, supondo que o qubit de destino seja inicializado 0.</span><span class="sxs-lookup"><span data-stu-id="d1d15-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="d1d15-106">A operação de adjoin pressupõe que o qubit de destino será redefinido como 0.</span><span class="sxs-lookup"><span data-stu-id="d1d15-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>  <span data-ttu-id="d1d15-107">Requer uma profundidade de RZ de 1, enquanto o número de qubits auxiliares é exponencial no número de qubits.</span><span class="sxs-lookup"><span data-stu-id="d1d15-107">Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.</span></span>

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="d1d15-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1d15-108">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="d1d15-109">controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d1d15-109">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d1d15-110">Qubits de controle</span><span class="sxs-lookup"><span data-stu-id="d1d15-110">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d1d15-111">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d1d15-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d1d15-112">Qubit de destino</span><span class="sxs-lookup"><span data-stu-id="d1d15-112">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="d1d15-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d1d15-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

