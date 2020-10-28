---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: Operação IncrementByInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: 363d48d697e3b2dad4d4896e6b1e701864649d9b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694783"
---
# <a name="incrementbyinteger-operation"></a><span data-ttu-id="67426-102">Operação IncrementByInteger</span><span class="sxs-lookup"><span data-stu-id="67426-102">IncrementByInteger operation</span></span>

<span data-ttu-id="67426-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="67426-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="67426-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="67426-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="67426-105">Incrementa um registro de Quantum não assinado por um inteiro clássico, usando rotações de fase.</span><span class="sxs-lookup"><span data-stu-id="67426-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="67426-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="67426-106">Description</span></span>

<span data-ttu-id="67426-107">Suponha que `target` o codifica um inteiro sem sinal $x $ em uma codificação little-endian e que `increment` seja igual a $a $.</span><span class="sxs-lookup"><span data-stu-id="67426-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="67426-108">Em seguida, essa operação implementa o unitário $ \ket{x} \mapsto \ket{x + a} $, em que a adição é executada módulo $2 ^ n $, em que $n = \texttt{Length (Target!)} $.</span><span class="sxs-lookup"><span data-stu-id="67426-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="67426-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="67426-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="67426-110">incremento: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="67426-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="67426-111">O inteiro pelo qual o `target` é incrementado por.</span><span class="sxs-lookup"><span data-stu-id="67426-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="67426-112">destino: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="67426-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="67426-113">Uma Quantum registra a codificação de um inteiro não assinado usando a codificação little-endian.</span><span class="sxs-lookup"><span data-stu-id="67426-113">A quantum register encoding an unsigned integer using little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="67426-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="67426-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

