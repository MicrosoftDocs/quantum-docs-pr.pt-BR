---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Operação quadrada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: 79a431d411c4ffd502fb5338b5396341fd63aea8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221854"
---
# <a name="squarei-operation"></a><span data-ttu-id="e3c10-102">Operação quadrada</span><span class="sxs-lookup"><span data-stu-id="e3c10-102">SquareI operation</span></span>

<span data-ttu-id="e3c10-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e3c10-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e3c10-104">Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="e3c10-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="e3c10-105">Computa o quadrado do inteiro `xs` em `result` , que deve ser inicialmente zero.</span><span class="sxs-lookup"><span data-stu-id="e3c10-105">Computes the square of the integer `xs` into `result`, which must be zero initially.</span></span>

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e3c10-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3c10-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="e3c10-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e3c10-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e3c10-108">número de $n de $ bits para quadrado (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e3c10-108">$n$-bit number to square (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="e3c10-109">resultado: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e3c10-109">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e3c10-110">o resultado de $2n $-bit (LittleEndian) deve estar no estado $ \ket {0} $ inicialmente.</span><span class="sxs-lookup"><span data-stu-id="e3c10-110">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e3c10-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e3c10-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e3c10-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3c10-112">Remarks</span></span>

<span data-ttu-id="e3c10-113">Usa uma abordagem Shift-and-add padrão para calcular o quadrado.</span><span class="sxs-lookup"><span data-stu-id="e3c10-113">Uses a standard shift-and-add approach to compute the square.</span></span> <span data-ttu-id="e3c10-114">Salva $n-$1 qubits em comparação com a solução direta, que primeiro copia XS antes de aplicar um multiplicador regular e, em seguida, desfazendo a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="e3c10-114">Saves $n-1$ qubits compared to the straight-forward solution which first copies out xs before applying a regular multiplier and then undoing the copy operation.</span></span>