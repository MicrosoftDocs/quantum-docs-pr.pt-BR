---
uid: Microsoft.Quantum.Canon.MultiplexOperationsBruteForceFromGenerator
title: Operação MultiplexOperationsBruteForceFromGenerator
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsBruteForceFromGenerator
qsharp.summary: >-
  Applies multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 2a9bb083b121745bd556aac692d5dc85ffec3791
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693958"
---
# <a name="multiplexoperationsbruteforcefromgenerator-operation"></a><span data-ttu-id="0b78c-102">Operação MultiplexOperationsBruteForceFromGenerator</span><span class="sxs-lookup"><span data-stu-id="0b78c-102">MultiplexOperationsBruteForceFromGenerator operation</span></span>

<span data-ttu-id="0b78c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0b78c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0b78c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0b78c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0b78c-105">Aplica a operação unitário controlada por multiplicação $U $ que aplica um $V unitário _j $ quando controlado pelo estado do número n-qubit $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="0b78c-105">Applies multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="0b78c-106">$U = \sum ^ {N-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="0b78c-106">$U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperationsBruteForceFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="0b78c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0b78c-107">Input</span></span>

### <a name="unitarygenerator--intint---t--unit-adj--ctl"></a><span data-ttu-id="0b78c-108">unitaryGenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> ' t => [unidade](xref:microsoft.quantum.lang-ref.unit) adj + CTL)</span><span class="sxs-lookup"><span data-stu-id="0b78c-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>

<span data-ttu-id="0b78c-109">Uma tupla em que o primeiro elemento `Int` é o número de unidades $N $, e o segundo elemento `(Int -> ('T => () is Adj + Ctl))` é uma função que usa um inteiro $j $ em $ [0, N-1] $ e gera a operação unitário $V _J $.</span><span class="sxs-lookup"><span data-stu-id="0b78c-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="0b78c-110">índice: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0b78c-110">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0b78c-111">$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="0b78c-111">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="0b78c-112">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="0b78c-112">target : 'T</span></span>

<span data-ttu-id="0b78c-113">Registro de qubit genérico que $V _j $ age em.</span><span class="sxs-lookup"><span data-stu-id="0b78c-113">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0b78c-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0b78c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0b78c-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="0b78c-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0b78c-116">T'</span><span class="sxs-lookup"><span data-stu-id="0b78c-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="0b78c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b78c-117">Remarks</span></span>

<span data-ttu-id="0b78c-118">`coefficients` será preenchido com elementos de identidade se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="0b78c-118">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="0b78c-119">Essa versão é implementada diretamente por meio de um loop por meio de operadores unitários controlados por n.</span><span class="sxs-lookup"><span data-stu-id="0b78c-119">This version is implemented directly by looping through n-controlled unitary operators.</span></span>