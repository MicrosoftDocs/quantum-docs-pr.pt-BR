---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledC
title: Operação ApplyMultiControlledC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledC
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 36010ba667190c237b64f60b7246010199a8ba1c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694265"
---
# <a name="applymulticontrolledc-operation"></a><span data-ttu-id="a3b75-102">Operação ApplyMultiControlledC</span><span class="sxs-lookup"><span data-stu-id="a3b75-102">ApplyMultiControlledC operation</span></span>

<span data-ttu-id="a3b75-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a3b75-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a3b75-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a3b75-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a3b75-105">Aplica uma versão controlada de multiplicação de uma operação controlada individualmente.</span><span class="sxs-lookup"><span data-stu-id="a3b75-105">Applies a multiply controlled version of a singly controlled operation.</span></span>
<span data-ttu-id="a3b75-106">O modificador `C` indica que a operação de qubit única é controlável.</span><span class="sxs-lookup"><span data-stu-id="a3b75-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyMultiControlledC (singlyControlledOp : (Qubit[] => Unit), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="a3b75-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3b75-107">Input</span></span>

### <a name="singlycontrolledop--qubit--unit"></a><span data-ttu-id="a3b75-108">singlyControlledOp: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="a3b75-108">singlyControlledOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a3b75-109">Uma operação controlada em um único qubit.</span><span class="sxs-lookup"><span data-stu-id="a3b75-109">An operation controlled on a single qubit.</span></span>
<span data-ttu-id="a3b75-110">Supõe-se que o primeiro qubit no argumento da operação seja um controle e que o resto seja de destino qubits.</span><span class="sxs-lookup"><span data-stu-id="a3b75-110">The first qubit in the argument of the operation is assumed to be a control and the rest are assumed to be target qubits.</span></span>
<span data-ttu-id="a3b75-111">`ApplyMultiControlled` sempre chama `singlyControlledOp` com um argumento de comprimento pelo menos 1.</span><span class="sxs-lookup"><span data-stu-id="a3b75-111">`ApplyMultiControlled` always calls `singlyControlledOp` with an argument of length at least 1.</span></span>


### <a name="ccnot--ccnotop"></a><span data-ttu-id="a3b75-112">ccnot: [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="a3b75-112">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="a3b75-113">A porta controlada por controlado não usada para a construção.</span><span class="sxs-lookup"><span data-stu-id="a3b75-113">The controlled-controlled-NOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="a3b75-114">controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a3b75-114">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a3b75-115">O qubits que deve `singlyControlledOp` ser controlado em.</span><span class="sxs-lookup"><span data-stu-id="a3b75-115">The qubits that `singlyControlledOp` is to be controlled on.</span></span>
<span data-ttu-id="a3b75-116">O comprimento de `controls` deve ser pelo menos 1.</span><span class="sxs-lookup"><span data-stu-id="a3b75-116">The length of `controls` must be at least 1.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="a3b75-117">destinos: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a3b75-117">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a3b75-118">O qubits de destino que `singlyControlledOp` atua.</span><span class="sxs-lookup"><span data-stu-id="a3b75-118">The target qubits that `singlyControlledOp` acts upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a3b75-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a3b75-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a3b75-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3b75-120">Remarks</span></span>

<span data-ttu-id="a3b75-121">Esta operação usa apenas qubits limpo ancilla.</span><span class="sxs-lookup"><span data-stu-id="a3b75-121">This operation uses only clean ancilla qubits.</span></span>

<span data-ttu-id="a3b75-122">Para obter a explicação e o diagrama de circuito, consulte a Figura 4,10, seção 4,3 em Nielsen & Chuang</span><span class="sxs-lookup"><span data-stu-id="a3b75-122">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang</span></span>

## <a name="references"></a><span data-ttu-id="a3b75-123">Referências</span><span class="sxs-lookup"><span data-stu-id="a3b75-123">References</span></span>

- [<span data-ttu-id="a3b75-124">*Michael A. Nielsen, Julio L. Chuang* , computação Quantum e informações de Quantum</span><span class="sxs-lookup"><span data-stu-id="a3b75-124"> *Michael A. Nielsen , Isaac L. Chuang* , Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a><span data-ttu-id="a3b75-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a3b75-125">See Also</span></span>

- [<span data-ttu-id="a3b75-126">Microsoft. Quantum. Canon. ApplyMultiControlledCA</span><span class="sxs-lookup"><span data-stu-id="a3b75-126">Microsoft.Quantum.Canon.ApplyMultiControlledCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyMultiControlledCA)