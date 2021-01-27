---
uid: Microsoft.Quantum.Canon.ApplyLowDepthAnd
title: Operação ApplyLowDepthAnd
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyLowDepthAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.
ms.openlocfilehash: 7fa9d9bf2f1905bf1b59e783d7bceb8cb2e09fa4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841699"
---
# <a name="applylowdepthand-operation"></a><span data-ttu-id="809c6-102">Operação ApplyLowDepthAnd</span><span class="sxs-lookup"><span data-stu-id="809c6-102">ApplyLowDepthAnd operation</span></span>

<span data-ttu-id="809c6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="809c6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="809c6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="809c6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="809c6-105">Inverte um determinado qubit de destino se e somente se ambos os controles qubits estiverem no estado 1, com T-depth 1, usando a medida para executar a operação de estado adjacente.</span><span class="sxs-lookup"><span data-stu-id="809c6-105">Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.</span></span>

```qsharp
operation ApplyLowDepthAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="809c6-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="809c6-106">Description</span></span>

<span data-ttu-id="809c6-107">Inverte `target` se e somente se ambos os controles forem 1, mas pressupõe que `target` está no estado 0.</span><span class="sxs-lookup"><span data-stu-id="809c6-107">Inverts `target` if and only if both controls are 1, but assumes that `target` is in state 0.</span></span>  <span data-ttu-id="809c6-108">A operação tem T-Count 4, T-depth 1 e requer um qubit auxiliar e, portanto, pode ser preferível a uma operação CCNOT, se `target` for conhecido como 0.</span><span class="sxs-lookup"><span data-stu-id="809c6-108">The operation has T-count 4, T-depth 1 and requires one helper qubit, and may therefore be preferable to a CCNOT operation, if `target` is known to be 0.</span></span>  <span data-ttu-id="809c6-109">O adjoin dessa operação é baseado em medição e não requer nenhuma Gates e nenhum qubit auxiliar.</span><span class="sxs-lookup"><span data-stu-id="809c6-109">The adjoint of this operation is measurement based and requires no T gates, and no helper qubit.</span></span>

## <a name="input"></a><span data-ttu-id="809c6-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="809c6-110">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="809c6-111">Control1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="809c6-111">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="809c6-112">Qubit de controle primeiro</span><span class="sxs-lookup"><span data-stu-id="809c6-112">First control qubit</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="809c6-113">Control2: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="809c6-113">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="809c6-114">Qubit de controle secundário</span><span class="sxs-lookup"><span data-stu-id="809c6-114">Second control qubit</span></span>


### <a name="target--qubit"></a><span data-ttu-id="809c6-115">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="809c6-115">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="809c6-116">Qubit auxiliar de destino; deve estar no estado 0</span><span class="sxs-lookup"><span data-stu-id="809c6-116">Target auxiliary qubit; must be in state 0</span></span>



## <a name="output--unit"></a><span data-ttu-id="809c6-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="809c6-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="809c6-118">Referências</span><span class="sxs-lookup"><span data-stu-id="809c6-118">References</span></span>

- <span data-ttu-id="809c6-119">Cody Jones: "construções de romance para a porta Toffoli tolerante a falhas", Phys. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/PhysRevA. 87.022328</span><span class="sxs-lookup"><span data-stu-id="809c6-119">Cody Jones: "Novel constructions for the fault-tolerant Toffoli gate", Phys. Rev. A 87, 022328, 2013 [arXiv:1212.5069](https://arxiv.org/abs/1212.5069) doi:10.1103/PhysRevA.87.022328</span></span>
- <span data-ttu-id="809c6-120">Peter Selinger: "circuitos Quantum de T-Depth One", Phys. Rev. A 87, 042302, 2013 [arXiv: 1210.0974](https://arxiv.org/abs/1210.0974) doi: 10.1103/PhysRevA. 87.042302</span><span class="sxs-lookup"><span data-stu-id="809c6-120">Peter Selinger: "Quantum circuits of T-depth one", Phys. Rev. A 87, 042302, 2013 [arXiv:1210.0974](https://arxiv.org/abs/1210.0974) doi:10.1103/PhysRevA.87.042302</span></span>