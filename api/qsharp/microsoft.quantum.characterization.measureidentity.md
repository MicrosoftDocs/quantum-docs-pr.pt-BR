---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Operação MeasureIdentity
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: 71a103fddb3a27703318975bea94bc7a22a9ce81
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693836"
---
# <a name="measureidentity-operation"></a><span data-ttu-id="9a997-102">Operação MeasureIdentity</span><span class="sxs-lookup"><span data-stu-id="9a997-102">MeasureIdentity operation</span></span>

<span data-ttu-id="9a997-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="9a997-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="9a997-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9a997-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9a997-105">Mede o operador de identidade em um registro de qubits.</span><span class="sxs-lookup"><span data-stu-id="9a997-105">Measures the identity operator on a register of qubits.</span></span>

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="9a997-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a997-106">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="9a997-107">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9a997-107">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9a997-108">O registro a ser medido.</span><span class="sxs-lookup"><span data-stu-id="9a997-108">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="9a997-109">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="9a997-109">Output : __invalid<Result>__</span></span>

<span data-ttu-id="9a997-110">O valor do resultado `Zero` .</span><span class="sxs-lookup"><span data-stu-id="9a997-110">The result value `Zero`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a997-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a997-111">Remarks</span></span>

<span data-ttu-id="9a997-112">Como $ \boldone $ tem apenas o eigenvalue $1 $ e não tem um eigenvalue negativo, essa operação sempre retorna `Zero` , correspondendo a eigenvalue $ + 1 = (-1) ^ 0 $ e não causa um recolhimento do estado de `register` .</span><span class="sxs-lookup"><span data-stu-id="9a997-112">Since $\boldone$ has only the eigenvalue $1$, and does not have a negative eigenvalue, this operation always returns `Zero`, corresponding to the eigenvalue $+1 = (-1)^0$, and does not cause a collapse of the state of `register`.</span></span>

<span data-ttu-id="9a997-113">Por si só, essa operação não é útil, mas é útil no contexto do processo tomography, pois fornece informações sobre a preservação de rastreamento de um processo Quantum.</span><span class="sxs-lookup"><span data-stu-id="9a997-113">On its own, this operation is not useful, but is helpful in the context of process tomography, as it provides information about the trace preservation of a quantum process.</span></span>
<span data-ttu-id="9a997-114">Em particular, um computador de destino com medição de perdas deve substituir essa operação por uma medida real de $ \boldone $.</span><span class="sxs-lookup"><span data-stu-id="9a997-114">In particular, a target machine with lossy measurement should replace this operation by an actual measurement of $\boldone$.</span></span>