---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledAnd
title: Operação ApplyMultiplyControlledAnd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.
ms.openlocfilehash: feca28d394e4af31eb4ffe737111d00ede45e27e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694263"
---
# <a name="applymultiplycontrolledand-operation"></a><span data-ttu-id="33ca2-102">Operação ApplyMultiplyControlledAnd</span><span class="sxs-lookup"><span data-stu-id="33ca2-102">ApplyMultiplyControlledAnd operation</span></span>

<span data-ttu-id="33ca2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="33ca2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="33ca2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="33ca2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="33ca2-105">Implementa um portão Toffoli com vários controle, supondo que o qubit de destino seja inicializado 0.</span><span class="sxs-lookup"><span data-stu-id="33ca2-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="33ca2-106">A operação de adjoin pressupõe que o qubit de destino será redefinido como 0.</span><span class="sxs-lookup"><span data-stu-id="33ca2-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>

```qsharp
operation ApplyMultiplyControlledAnd (controls : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="33ca2-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="33ca2-107">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="33ca2-108">controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="33ca2-108">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="33ca2-109">Qubits de controle</span><span class="sxs-lookup"><span data-stu-id="33ca2-109">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="33ca2-110">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="33ca2-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="33ca2-111">Qubit de destino</span><span class="sxs-lookup"><span data-stu-id="33ca2-111">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="33ca2-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="33ca2-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

