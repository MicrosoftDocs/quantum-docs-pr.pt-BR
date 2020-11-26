---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledAnd
title: Operação ApplyMultiplyControlledAnd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.
ms.openlocfilehash: 17a757278500833bc5a5d0635af020cfe1fd569f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218386"
---
# <a name="applymultiplycontrolledand-operation"></a><span data-ttu-id="208b0-102">Operação ApplyMultiplyControlledAnd</span><span class="sxs-lookup"><span data-stu-id="208b0-102">ApplyMultiplyControlledAnd operation</span></span>

<span data-ttu-id="208b0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="208b0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="208b0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="208b0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="208b0-105">Implementa um portão Toffoli com vários controle, supondo que o qubit de destino seja inicializado 0.</span><span class="sxs-lookup"><span data-stu-id="208b0-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="208b0-106">A operação de adjoin pressupõe que o qubit de destino será redefinido como 0.</span><span class="sxs-lookup"><span data-stu-id="208b0-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>

```qsharp
operation ApplyMultiplyControlledAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="208b0-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="208b0-107">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="208b0-108">controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="208b0-108">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="208b0-109">Qubits de controle</span><span class="sxs-lookup"><span data-stu-id="208b0-109">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="208b0-110">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="208b0-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="208b0-111">Qubit de destino</span><span class="sxs-lookup"><span data-stu-id="208b0-111">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="208b0-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="208b0-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

