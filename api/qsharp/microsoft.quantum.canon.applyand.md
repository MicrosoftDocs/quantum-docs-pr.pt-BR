---
uid: Microsoft.Quantum.Canon.ApplyAnd
title: Operação Clicarei
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.
ms.openlocfilehash: 5a4e18cb0361708e1fc00e8d62c0a6c2415d6bed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694341"
---
# <a name="applyand-operation"></a><span data-ttu-id="e8d52-102">Operação Clicarei</span><span class="sxs-lookup"><span data-stu-id="e8d52-102">ApplyAnd operation</span></span>

<span data-ttu-id="e8d52-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8d52-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8d52-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e8d52-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e8d52-105">Inverte um determinado qubit de destino se e somente se ambos os controles qubits estiverem no estado 1, usando a medida para executar a operação de adjoin.</span><span class="sxs-lookup"><span data-stu-id="e8d52-105">Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.</span></span>

```qsharp
operation ApplyAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="e8d52-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8d52-106">Description</span></span>

<span data-ttu-id="e8d52-107">Inverte `target` se e somente se ambos os controles forem 1, mas pressupõe que `target` está no estado 0.</span><span class="sxs-lookup"><span data-stu-id="e8d52-107">Inverts `target` if and only if both controls are 1, but assumes that `target` is in state 0.</span></span>  <span data-ttu-id="e8d52-108">A operação tem T-Count 4, T-Depth 2 e não requer nenhum qubit auxiliar e, portanto, pode ser preferível a uma operação CCNOT, se `target` for conhecido como 0.</span><span class="sxs-lookup"><span data-stu-id="e8d52-108">The operation has T-count 4, T-depth 2 and requires no helper qubit, and may therefore be preferable to a CCNOT operation, if `target` is known to be 0.</span></span>  <span data-ttu-id="e8d52-109">O adjoin dessa operação é baseado em medição e não requer nenhuma Gates.</span><span class="sxs-lookup"><span data-stu-id="e8d52-109">The adjoint of this operation is measurement based and requires no T gates.</span></span>

<span data-ttu-id="e8d52-110">O aplicativo controlado desta operação não requer nenhum auxiliar qubit, `2^c` `Rz` Gates e não é otimizado para profundidade, em que `c` é o número de qubits de controle geral, incluindo os dois controles da `ApplyAnd` operação.</span><span class="sxs-lookup"><span data-stu-id="e8d52-110">The controlled application of this operation requires no helper qubit, `2^c` `Rz` gates and is not optimized for depth, where `c` is the number of overall control qubits including the two controls from the `ApplyAnd` operation.</span></span>  <span data-ttu-id="e8d52-111">O aplicativo controlado por adjacente requer `2^c - 1` `Rz` Gates (com um ângulo duas vezes o tamanho da operação não-adjacente), nenhum auxiliar qubit e não é otimizado para profundidade.</span><span class="sxs-lookup"><span data-stu-id="e8d52-111">The adjoint controlled application requires `2^c - 1` `Rz` gates (with an angle twice the size of the non-adjoint operation), no helper qubit and is not optimized for depth.</span></span>

## <a name="input"></a><span data-ttu-id="e8d52-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8d52-112">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="e8d52-113">Control1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e8d52-113">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e8d52-114">Qubit de controle primeiro</span><span class="sxs-lookup"><span data-stu-id="e8d52-114">First control qubit</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="e8d52-115">Control2: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e8d52-115">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e8d52-116">Qubit de controle secundário</span><span class="sxs-lookup"><span data-stu-id="e8d52-116">Second control qubit</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e8d52-117">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e8d52-117">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e8d52-118">Qubit auxiliar de destino; deve estar no estado 0</span><span class="sxs-lookup"><span data-stu-id="e8d52-118">Target auxiliary qubit; must be in state 0</span></span>



## <a name="output--unit"></a><span data-ttu-id="e8d52-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8d52-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="e8d52-120">Referências</span><span class="sxs-lookup"><span data-stu-id="e8d52-120">References</span></span>

- <span data-ttu-id="e8d52-121">Cody Jones: "construções de romance para a porta Toffoli tolerante a falhas", Phys. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/PhysRevA. 87.022328</span><span class="sxs-lookup"><span data-stu-id="e8d52-121">Cody Jones: "Novel constructions for the fault-tolerant Toffoli gate", Phys. Rev. A 87, 022328, 2013 [arXiv:1212.5069](https://arxiv.org/abs/1212.5069) doi:10.1103/PhysRevA.87.022328</span></span>
- <span data-ttu-id="e8d52-122">Craig Gidney: "metade do custo da adição da Quantum", Quantum 2, página 74, 2018 [arXiv: 1709.06648](https://arxiv.org/abs/1709.06648) doi: 10.1103/PhysRevA. 85.044302</span><span class="sxs-lookup"><span data-stu-id="e8d52-122">Craig Gidney: "Halving the cost of quantum addition", Quantum 2, page 74, 2018 [arXiv:1709.06648](https://arxiv.org/abs/1709.06648) doi:10.1103/PhysRevA.85.044302</span></span>
- <span data-ttu-id="e8d52-123">Mathias Soeken: "circuitos do Oracle Quantum e padrão de árvore de Natal", [artigo de blog de 19 de dezembro de 2019](https://msoeken.github.io/blog_qac.html) (Observação: explica a construção de vários controlados)</span><span class="sxs-lookup"><span data-stu-id="e8d52-123">Mathias Soeken: "Quantum Oracle Circuits and the Christmas Tree Pattern", [Blog article from December 19, 2019](https://msoeken.github.io/blog_qac.html) (note: explains the multiple controlled construction)</span></span>