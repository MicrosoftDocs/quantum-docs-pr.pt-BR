---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Operação ApplyFermionicSWAP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 0c470705843a6360df0a72374570d86571397e41
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218794"
---
# <a name="applyfermionicswap-operation"></a><span data-ttu-id="cbad5-102">Operação ApplyFermionicSWAP</span><span class="sxs-lookup"><span data-stu-id="cbad5-102">ApplyFermionicSWAP operation</span></span>

<span data-ttu-id="cbad5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cbad5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cbad5-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cbad5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cbad5-105">Aplica a permuta Fermionic.</span><span class="sxs-lookup"><span data-stu-id="cbad5-105">Applies the Fermionic SWAP.</span></span>

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="cbad5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbad5-106">Description</span></span>

<span data-ttu-id="cbad5-107">Isso, essencialmente, troca o qubits enquanto aplica uma fase global de-1 se ambos os qubits são 1s.</span><span class="sxs-lookup"><span data-stu-id="cbad5-107">This essentially swaps the qubits while applying a global phase of -1 if both qubits are 1s.</span></span> <span data-ttu-id="cbad5-108">Preserva symmetrization de órbitas.</span><span class="sxs-lookup"><span data-stu-id="cbad5-108">Preserves anti-symmetrization of orbitals.</span></span>
<span data-ttu-id="cbad5-109">Consulte  para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="cbad5-109">See  for more information.</span></span>

<span data-ttu-id="cbad5-110">Esta operação é representada pelo operador unitário \begin{align} f_ {swap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-1 \\ \\ \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="cbad5-110">This operation is represented by the unitary operator \begin{align} f_{swap} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -1 \\\\ \end{bmatrix}.</span></span>
<span data-ttu-id="cbad5-111">\end{align}</span><span class="sxs-lookup"><span data-stu-id="cbad5-111">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="cbad5-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbad5-112">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="cbad5-113">qubit1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cbad5-113">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cbad5-114">O primeiro qubit a ser trocado.</span><span class="sxs-lookup"><span data-stu-id="cbad5-114">The first qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="cbad5-115">qubit2: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cbad5-115">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cbad5-116">O segundo qubit a ser trocado.</span><span class="sxs-lookup"><span data-stu-id="cbad5-116">The second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cbad5-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cbad5-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="cbad5-118">Referências</span><span class="sxs-lookup"><span data-stu-id="cbad5-118">References</span></span>

- [<span data-ttu-id="cbad5-119">*Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic canal*, arXiv: 1706.00023</span><span class="sxs-lookup"><span data-stu-id="cbad5-119"> *Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic Chan*, arXiv:1706.00023 </span></span>](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a><span data-ttu-id="cbad5-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cbad5-120">See Also</span></span>

- [<span data-ttu-id="cbad5-121">Microsoft. Quantum. intrínseco. SWAP</span><span class="sxs-lookup"><span data-stu-id="cbad5-121">Microsoft.Quantum.Intrinsic.SWAP</span></span>](xref:Microsoft.Quantum.Intrinsic.SWAP)