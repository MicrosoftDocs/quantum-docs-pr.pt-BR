---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Operação quadrada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: 6813c8144b0ac98bae404b5e9b97e08b06c6bb3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846307"
---
# <a name="squarei-operation"></a><span data-ttu-id="0cb49-102">Operação quadrada</span><span class="sxs-lookup"><span data-stu-id="0cb49-102">SquareI operation</span></span>

<span data-ttu-id="0cb49-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0cb49-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0cb49-104">Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="0cb49-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="0cb49-105">Computa o quadrado do inteiro `xs` em `result` , que deve ser inicialmente zero.</span><span class="sxs-lookup"><span data-stu-id="0cb49-105">Computes the square of the integer `xs` into `result`, which must be zero initially.</span></span>

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0cb49-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0cb49-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="0cb49-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0cb49-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0cb49-108">número de $n de $ bits para quadrado (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0cb49-108">$n$-bit number to square (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="0cb49-109">resultado: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0cb49-109">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0cb49-110">o resultado de $2n $-bit (LittleEndian) deve estar no estado $ \ket {0} $ inicialmente.</span><span class="sxs-lookup"><span data-stu-id="0cb49-110">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0cb49-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0cb49-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0cb49-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cb49-112">Remarks</span></span>

<span data-ttu-id="0cb49-113">Usa uma abordagem Shift-and-add padrão para calcular o quadrado.</span><span class="sxs-lookup"><span data-stu-id="0cb49-113">Uses a standard shift-and-add approach to compute the square.</span></span> <span data-ttu-id="0cb49-114">Salva $n-$1 qubits em comparação com a solução direta, que primeiro copia XS antes de aplicar um multiplicador regular e, em seguida, desfazendo a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="0cb49-114">Saves $n-1$ qubits compared to the straight-forward solution which first copies out xs before applying a regular multiplier and then undoing the copy operation.</span></span>