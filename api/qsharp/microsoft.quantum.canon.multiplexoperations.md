---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: Operação MultiplexOperations
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 267c9c2858090ebe024fd387938e8bd2f8c76867
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693960"
---
# <a name="multiplexoperations-operation"></a><span data-ttu-id="738e0-102">Operação MultiplexOperations</span><span class="sxs-lookup"><span data-stu-id="738e0-102">MultiplexOperations operation</span></span>

<span data-ttu-id="738e0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="738e0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="738e0-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="738e0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="738e0-105">Aplica uma matriz de operações controladas por uma matriz de Estados de número.</span><span class="sxs-lookup"><span data-stu-id="738e0-105">Applies an array of operations controlled by an array of number states.</span></span>

<span data-ttu-id="738e0-106">Ou seja, aplica a operação unitário controlada por multiplicação $U $ que aplica um $V unitário _j $ quando controlado $n pelo estado do número $ qubit $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="738e0-106">That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="738e0-107">$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="738e0-107">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="738e0-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="738e0-108">Input</span></span>

### <a name="unitaries--t--unit-adj--ctl"></a><span data-ttu-id="738e0-109">unidades: não => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL []</span><span class="sxs-lookup"><span data-stu-id="738e0-109">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>

<span data-ttu-id="738e0-110">Matriz de até $2 ^ n $ operações de unitário.</span><span class="sxs-lookup"><span data-stu-id="738e0-110">Array of up to $2^n$ unitary operations.</span></span> <span data-ttu-id="738e0-111">A operação $j $ th é indexada pelo estado do número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="738e0-111">The $j$th operation is indexed by the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="738e0-112">índice: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="738e0-112">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="738e0-113">$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="738e0-113">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="738e0-114">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="738e0-114">target : 'T</span></span>

<span data-ttu-id="738e0-115">Registro de qubit genérico que $V _j $ age em.</span><span class="sxs-lookup"><span data-stu-id="738e0-115">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="738e0-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="738e0-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="738e0-117">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="738e0-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="738e0-118">T'</span><span class="sxs-lookup"><span data-stu-id="738e0-118">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="738e0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="738e0-119">Remarks</span></span>

<span data-ttu-id="738e0-120">`coefficients` será preenchido com elementos de identidade se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="738e0-120">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="738e0-121">Essa implementação usa $n auxiliar qubits-$1.</span><span class="sxs-lookup"><span data-stu-id="738e0-121">This implementation uses $n - 1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="738e0-122">Referências</span><span class="sxs-lookup"><span data-stu-id="738e0-122">References</span></span>

- <span data-ttu-id="738e0-123">Para a primeira simulação de Quantum com aumento de velocidade Quantum Andrew M. Childs, Dmitri Maslov, Yunseong, Neil J. Ross, iuan Su https://arxiv.org/abs/1711.10980</span><span class="sxs-lookup"><span data-stu-id="738e0-123">Toward the first quantum simulation with quantum speedup Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su https://arxiv.org/abs/1711.10980</span></span>