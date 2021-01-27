---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Operação ApplyFermionicSWAP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 334f407a32dabc8f4e0a1a29c8f06a1b9f40dc59
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845047"
---
# <a name="applyfermionicswap-operation"></a><span data-ttu-id="af9f6-102">Operação ApplyFermionicSWAP</span><span class="sxs-lookup"><span data-stu-id="af9f6-102">ApplyFermionicSWAP operation</span></span>

<span data-ttu-id="af9f6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="af9f6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="af9f6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="af9f6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="af9f6-105">Aplica a permuta Fermionic.</span><span class="sxs-lookup"><span data-stu-id="af9f6-105">Applies the Fermionic SWAP.</span></span>

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="af9f6-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="af9f6-106">Description</span></span>

<span data-ttu-id="af9f6-107">Isso, essencialmente, troca o qubits enquanto aplica uma fase global de-1 se ambos os qubits são 1s.</span><span class="sxs-lookup"><span data-stu-id="af9f6-107">This essentially swaps the qubits while applying a global phase of -1 if both qubits are 1s.</span></span> <span data-ttu-id="af9f6-108">Preserva symmetrization de órbitas.</span><span class="sxs-lookup"><span data-stu-id="af9f6-108">Preserves anti-symmetrization of orbitals.</span></span>
<span data-ttu-id="af9f6-109">Consulte  para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="af9f6-109">See  for more information.</span></span>

<span data-ttu-id="af9f6-110">Esta operação é representada pelo operador unitário \begin{align} f_ {swap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-1 \\ \\ \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="af9f6-110">This operation is represented by the unitary operator \begin{align} f_{swap} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -1 \\\\ \end{bmatrix}.</span></span>
<span data-ttu-id="af9f6-111">\end{align}</span><span class="sxs-lookup"><span data-stu-id="af9f6-111">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="af9f6-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="af9f6-112">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="af9f6-113">qubit1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="af9f6-113">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="af9f6-114">O primeiro qubit a ser trocado.</span><span class="sxs-lookup"><span data-stu-id="af9f6-114">The first qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="af9f6-115">qubit2: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="af9f6-115">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="af9f6-116">O segundo qubit a ser trocado.</span><span class="sxs-lookup"><span data-stu-id="af9f6-116">The second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="af9f6-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="af9f6-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="af9f6-118">Referências</span><span class="sxs-lookup"><span data-stu-id="af9f6-118">References</span></span>

- [<span data-ttu-id="af9f6-119">*Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic canal*, arXiv: 1706.00023</span><span class="sxs-lookup"><span data-stu-id="af9f6-119"> *Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic Chan*, arXiv:1706.00023 </span></span>](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a><span data-ttu-id="af9f6-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="af9f6-120">See Also</span></span>

- [<span data-ttu-id="af9f6-121">Microsoft. Quantum. intrínseco. SWAP</span><span class="sxs-lookup"><span data-stu-id="af9f6-121">Microsoft.Quantum.Intrinsic.SWAP</span></span>](xref:Microsoft.Quantum.Intrinsic.SWAP)