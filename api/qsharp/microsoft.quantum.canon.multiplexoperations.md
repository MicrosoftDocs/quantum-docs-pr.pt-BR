---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: Operação MultiplexOperations
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 1cf483bb0d3b7cc43d271b65a2363fab95ff0f3b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852539"
---
# <a name="multiplexoperations-operation"></a><span data-ttu-id="18660-102">Operação MultiplexOperations</span><span class="sxs-lookup"><span data-stu-id="18660-102">MultiplexOperations operation</span></span>

<span data-ttu-id="18660-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="18660-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="18660-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="18660-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="18660-105">Aplica uma matriz de operações controladas por uma matriz de Estados de número.</span><span class="sxs-lookup"><span data-stu-id="18660-105">Applies an array of operations controlled by an array of number states.</span></span>

<span data-ttu-id="18660-106">Ou seja, aplica a operação unitário controlada por multiplicação $U $ que aplica um $V unitário _j $ quando controlado $n pelo estado do número $ qubit $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="18660-106">That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="18660-107">$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="18660-107">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="18660-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="18660-108">Input</span></span>

### <a name="unitaries--t--unit--is-adj--ctl"></a><span data-ttu-id="18660-109">unidades: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL []</span><span class="sxs-lookup"><span data-stu-id="18660-109">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="18660-110">Matriz de até $2 ^ n $ operações de unitário.</span><span class="sxs-lookup"><span data-stu-id="18660-110">Array of up to $2^n$ unitary operations.</span></span> <span data-ttu-id="18660-111">A operação $j $ th é indexada pelo estado do número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="18660-111">The $j$th operation is indexed by the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="18660-112">índice: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="18660-112">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="18660-113">$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="18660-113">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="18660-114">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="18660-114">target : 'T</span></span>

<span data-ttu-id="18660-115">Registro de qubit genérico que $V _j $ age em.</span><span class="sxs-lookup"><span data-stu-id="18660-115">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="18660-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="18660-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="18660-117">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="18660-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="18660-118">T'</span><span class="sxs-lookup"><span data-stu-id="18660-118">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="18660-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="18660-119">Remarks</span></span>

<span data-ttu-id="18660-120">`coefficients` será preenchido com elementos de identidade se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="18660-120">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="18660-121">Essa implementação usa $n auxiliar qubits-$1.</span><span class="sxs-lookup"><span data-stu-id="18660-121">This implementation uses $n - 1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="18660-122">Referências</span><span class="sxs-lookup"><span data-stu-id="18660-122">References</span></span>

- <span data-ttu-id="18660-123">Para a primeira simulação de Quantum com aumento de velocidade Quantum Andrew M. Childs, Dmitri Maslov, Yunseong, Neil J. Ross, iuan Su https://arxiv.org/abs/1711.10980</span><span class="sxs-lookup"><span data-stu-id="18660-123">Toward the first quantum simulation with quantum speedup Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su https://arxiv.org/abs/1711.10980</span></span>