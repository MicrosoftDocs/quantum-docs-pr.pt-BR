---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledC
title: Operação ApplyMultiControlledC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledC
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: bf6b78cd18a827a9a4fd9d61dfd4d240de3503e9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844859"
---
# <a name="applymulticontrolledc-operation"></a><span data-ttu-id="04849-102">Operação ApplyMultiControlledC</span><span class="sxs-lookup"><span data-stu-id="04849-102">ApplyMultiControlledC operation</span></span>

<span data-ttu-id="04849-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="04849-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="04849-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="04849-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="04849-105">Aplica uma versão controlada de multiplicação de uma operação controlada individualmente.</span><span class="sxs-lookup"><span data-stu-id="04849-105">Applies a multiply controlled version of a singly controlled operation.</span></span>
<span data-ttu-id="04849-106">O modificador `C` indica que a operação de qubit única é controlável.</span><span class="sxs-lookup"><span data-stu-id="04849-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyMultiControlledC (singlyControlledOp : (Qubit[] => Unit), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="04849-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="04849-107">Input</span></span>

### <a name="singlycontrolledop--qubit--unit"></a><span data-ttu-id="04849-108">singlyControlledOp: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="04849-108">singlyControlledOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="04849-109">Uma operação controlada em um único qubit.</span><span class="sxs-lookup"><span data-stu-id="04849-109">An operation controlled on a single qubit.</span></span>
<span data-ttu-id="04849-110">Supõe-se que o primeiro qubit no argumento da operação seja um controle e que o resto seja de destino qubits.</span><span class="sxs-lookup"><span data-stu-id="04849-110">The first qubit in the argument of the operation is assumed to be a control and the rest are assumed to be target qubits.</span></span>
<span data-ttu-id="04849-111">`ApplyMultiControlled` sempre chama `singlyControlledOp` com um argumento de comprimento pelo menos 1.</span><span class="sxs-lookup"><span data-stu-id="04849-111">`ApplyMultiControlled` always calls `singlyControlledOp` with an argument of length at least 1.</span></span>


### <a name="ccnot--ccnotop"></a><span data-ttu-id="04849-112">ccnot: [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="04849-112">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="04849-113">A porta controlada por controlado não usada para a construção.</span><span class="sxs-lookup"><span data-stu-id="04849-113">The controlled-controlled-NOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="04849-114">controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="04849-114">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="04849-115">O qubits que deve `singlyControlledOp` ser controlado em.</span><span class="sxs-lookup"><span data-stu-id="04849-115">The qubits that `singlyControlledOp` is to be controlled on.</span></span>
<span data-ttu-id="04849-116">O comprimento de `controls` deve ser pelo menos 1.</span><span class="sxs-lookup"><span data-stu-id="04849-116">The length of `controls` must be at least 1.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="04849-117">destinos: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="04849-117">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="04849-118">O qubits de destino que `singlyControlledOp` atua.</span><span class="sxs-lookup"><span data-stu-id="04849-118">The target qubits that `singlyControlledOp` acts upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="04849-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="04849-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="04849-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="04849-120">Remarks</span></span>

<span data-ttu-id="04849-121">Esta operação usa apenas qubits limpo ancilla.</span><span class="sxs-lookup"><span data-stu-id="04849-121">This operation uses only clean ancilla qubits.</span></span>

<span data-ttu-id="04849-122">Para obter a explicação e o diagrama de circuito, consulte a Figura 4,10, seção 4,3 em Nielsen & Chuang</span><span class="sxs-lookup"><span data-stu-id="04849-122">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang</span></span>

## <a name="references"></a><span data-ttu-id="04849-123">Referências</span><span class="sxs-lookup"><span data-stu-id="04849-123">References</span></span>

- [<span data-ttu-id="04849-124">*Michael A. Nielsen, Julio L. Chuang*, computação Quantum e informações de Quantum</span><span class="sxs-lookup"><span data-stu-id="04849-124"> *Michael A. Nielsen , Isaac L. Chuang*, Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a><span data-ttu-id="04849-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="04849-125">See Also</span></span>

- [<span data-ttu-id="04849-126">Microsoft. Quantum. Canon. ApplyMultiControlledCA</span><span class="sxs-lookup"><span data-stu-id="04849-126">Microsoft.Quantum.Canon.ApplyMultiControlledCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyMultiControlledCA)