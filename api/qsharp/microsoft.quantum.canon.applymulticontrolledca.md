---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: Operação ApplyMultiControlledCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: a6549084b1c2fda885823f451d17f9c2ebbb4600
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841688"
---
# <a name="applymulticontrolledca-operation"></a><span data-ttu-id="e0ba2-102">Operação ApplyMultiControlledCA</span><span class="sxs-lookup"><span data-stu-id="e0ba2-102">ApplyMultiControlledCA operation</span></span>

<span data-ttu-id="e0ba2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e0ba2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e0ba2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e0ba2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e0ba2-105">Aplica uma versão controlada de multiplicação de uma operação controlada individualmente.</span><span class="sxs-lookup"><span data-stu-id="e0ba2-105">Applies a multiply controlled version of a singly controlled operation.</span></span>
<span data-ttu-id="e0ba2-106">O modificador `CA` indica que a operação single-qubit é controlável e adjointable.</span><span class="sxs-lookup"><span data-stu-id="e0ba2-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyMultiControlledCA (singlyControlledOp : (Qubit[] => Unit is Adj), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e0ba2-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0ba2-107">Input</span></span>

### <a name="singlycontrolledop--qubit--unit--is-adj"></a><span data-ttu-id="e0ba2-108">singlyControlledOp: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj</span><span class="sxs-lookup"><span data-stu-id="e0ba2-108">singlyControlledOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e0ba2-109">Uma operação controlada em um único qubit.</span><span class="sxs-lookup"><span data-stu-id="e0ba2-109">An operation controlled on a single qubit.</span></span>
<span data-ttu-id="e0ba2-110">O primeiro qubit no argumento da operação assumida como um controle e o restante são considerados como destino qubits.</span><span class="sxs-lookup"><span data-stu-id="e0ba2-110">The first qubit in the argument of the operation assumed to be a control and the rest are assumed to be target qubits.</span></span>
<span data-ttu-id="e0ba2-111">`ApplyMultiControlled` sempre chama `singlyControlledOp` com um argumento de comprimento pelo menos 1.</span><span class="sxs-lookup"><span data-stu-id="e0ba2-111">`ApplyMultiControlled` always calls `singlyControlledOp` with an argument of length at least 1.</span></span>


### <a name="ccnot--ccnotop"></a><span data-ttu-id="e0ba2-112">ccnot: [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="e0ba2-112">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="e0ba2-113">A porta controlada por controlado não usada para a construção.</span><span class="sxs-lookup"><span data-stu-id="e0ba2-113">The controlled-controlled-NOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="e0ba2-114">controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e0ba2-114">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e0ba2-115">O qubits que deve `singlyControlledOp` ser controlado em.</span><span class="sxs-lookup"><span data-stu-id="e0ba2-115">The qubits that `singlyControlledOp` is to be controlled on.</span></span>
<span data-ttu-id="e0ba2-116">O comprimento de `controls` deve ser pelo menos 1.</span><span class="sxs-lookup"><span data-stu-id="e0ba2-116">The length of `controls` must be at least 1.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="e0ba2-117">destinos: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e0ba2-117">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e0ba2-118">O qubits de destino que `singlyControlledOp` atua.</span><span class="sxs-lookup"><span data-stu-id="e0ba2-118">The target qubits that `singlyControlledOp` acts upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e0ba2-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e0ba2-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e0ba2-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0ba2-120">Remarks</span></span>

<span data-ttu-id="e0ba2-121">Esta operação usa apenas qubits limpo ancilla.</span><span class="sxs-lookup"><span data-stu-id="e0ba2-121">This operation uses only clean ancilla qubits.</span></span>

<span data-ttu-id="e0ba2-122">Para obter a explicação e o diagrama de circuito, consulte a Figura 4,10, seção 4,3 em Nielsen & Chuang</span><span class="sxs-lookup"><span data-stu-id="e0ba2-122">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang</span></span>

## <a name="references"></a><span data-ttu-id="e0ba2-123">Referências</span><span class="sxs-lookup"><span data-stu-id="e0ba2-123">References</span></span>

- [<span data-ttu-id="e0ba2-124">*Michael A. Nielsen, Julio L. Chuang*, computação Quantum e informações de Quantum</span><span class="sxs-lookup"><span data-stu-id="e0ba2-124"> *Michael A. Nielsen , Isaac L. Chuang*, Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a><span data-ttu-id="e0ba2-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e0ba2-125">See Also</span></span>

- [<span data-ttu-id="e0ba2-126">Microsoft. Quantum. Canon. ApplyMultiControlledC</span><span class="sxs-lookup"><span data-stu-id="e0ba2-126">Microsoft.Quantum.Canon.ApplyMultiControlledC</span></span>](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)