---
uid: Microsoft.Quantum.Canon.ApplyCCNOTChain
title: Operação ApplyCCNOTChain
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCCNOTChain
qsharp.summary: Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers. Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.
ms.openlocfilehash: e4f38e9bb54839076b817f6e61e96ca6a550576b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694329"
---
# <a name="applyccnotchain-operation"></a><span data-ttu-id="da20e-102">Operação ApplyCCNOTChain</span><span class="sxs-lookup"><span data-stu-id="da20e-102">ApplyCCNOTChain operation</span></span>

<span data-ttu-id="da20e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="da20e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="da20e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="da20e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="da20e-105">Implementa uma cascata de CCNOT Gates controladas em bits correspondentes de dois registros qubit, agindo na próxima qubit de um dos registros.</span><span class="sxs-lookup"><span data-stu-id="da20e-105">Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers.</span></span>
<span data-ttu-id="da20e-106">A partir do qubits na posição 0 em ambos os registros como controles, CCNOT é aplicado ao qubit na posição 1 do registro de destino, então controlado pelo qubits na posição 1 atuando no qubit na posição 2 no registro de destino, etc., terminando com uma ação no qubit de destino na posição `Length(nQubits)-1` .</span><span class="sxs-lookup"><span data-stu-id="da20e-106">Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.</span></span>

```qsharp
operation ApplyCCNOTChain (register : Qubit[], targets : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="da20e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="da20e-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="da20e-108">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="da20e-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="da20e-109">Registro de qubit, usado somente para controles.</span><span class="sxs-lookup"><span data-stu-id="da20e-109">Qubit register, only used for controls.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="da20e-110">destinos: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="da20e-110">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="da20e-111">Registro de qubit, usado para controles e como destino.</span><span class="sxs-lookup"><span data-stu-id="da20e-111">Qubit register, used for controls and as target.</span></span>



## <a name="output--unit"></a><span data-ttu-id="da20e-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="da20e-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="da20e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="da20e-113">Remarks</span></span>

<span data-ttu-id="da20e-114">O registro qubit de destino deve ter um qubit mais do que o outro registro.</span><span class="sxs-lookup"><span data-stu-id="da20e-114">The target qubit register must have one qubit more than the other register.</span></span>