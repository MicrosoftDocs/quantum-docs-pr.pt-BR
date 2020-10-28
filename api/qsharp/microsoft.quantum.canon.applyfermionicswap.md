---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Operação ApplyFermionicSWAP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 25dd91b200700d1474cf27bf1d0fa71d57f2e09b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694310"
---
# <a name="applyfermionicswap-operation"></a><span data-ttu-id="3945e-102">Operação ApplyFermionicSWAP</span><span class="sxs-lookup"><span data-stu-id="3945e-102">ApplyFermionicSWAP operation</span></span>

<span data-ttu-id="3945e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3945e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3945e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3945e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3945e-105">Aplica a permuta Fermionic.</span><span class="sxs-lookup"><span data-stu-id="3945e-105">Applies the Fermionic SWAP.</span></span>

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="3945e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3945e-106">Description</span></span>

<span data-ttu-id="3945e-107">Isso, essencialmente, troca o qubits enquanto aplica uma fase global de-1 se ambos os qubits são 1s.</span><span class="sxs-lookup"><span data-stu-id="3945e-107">This essentially swaps the qubits while applying a global phase of -1 if both qubits are 1s.</span></span> <span data-ttu-id="3945e-108">Preserva symmetrization de órbitas.</span><span class="sxs-lookup"><span data-stu-id="3945e-108">Preserves anti-symmetrization of orbitals.</span></span>
<span data-ttu-id="3945e-109">Consulte  para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3945e-109">See  for more information.</span></span>

<span data-ttu-id="3945e-110">Esta operação é representada pelo operador unitário \begin{align} f_ {swap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-1 \\ \\ \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="3945e-110">This operation is represented by the unitary operator \begin{align} f_{swap} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -1 \\\\ \end{bmatrix}.</span></span>
<span data-ttu-id="3945e-111">\end{align}</span><span class="sxs-lookup"><span data-stu-id="3945e-111">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="3945e-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="3945e-112">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="3945e-113">qubit1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3945e-113">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3945e-114">O primeiro qubit a ser trocado.</span><span class="sxs-lookup"><span data-stu-id="3945e-114">The first qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="3945e-115">qubit2: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3945e-115">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3945e-116">O segundo qubit a ser trocado.</span><span class="sxs-lookup"><span data-stu-id="3945e-116">The second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3945e-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3945e-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="3945e-118">Referências</span><span class="sxs-lookup"><span data-stu-id="3945e-118">References</span></span>

- [<span data-ttu-id="3945e-119">*Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic canal* , arXiv: 1706.00023</span><span class="sxs-lookup"><span data-stu-id="3945e-119"> *Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic Chan* , arXiv:1706.00023 </span></span>](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a><span data-ttu-id="3945e-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3945e-120">See Also</span></span>

- [<span data-ttu-id="3945e-121">Microsoft. Quantum. intrínseco. SWAP</span><span class="sxs-lookup"><span data-stu-id="3945e-121">Microsoft.Quantum.Intrinsic.SWAP</span></span>](xref:Microsoft.Quantum.Intrinsic.SWAP)