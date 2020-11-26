---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: Operação de multiplicação
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 96922f0147788b37cc9bace5154288a722d4ba95
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222500"
---
# <a name="multiplyi-operation"></a><span data-ttu-id="19817-102">Operação de multiplicação</span><span class="sxs-lookup"><span data-stu-id="19817-102">MultiplyI operation</span></span>

<span data-ttu-id="19817-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="19817-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="19817-104">Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="19817-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="19817-105">Multiplique inteiro `xs` por inteiro `ys` e armazene o resultado em `result` , que deve ser inicialmente zero.</span><span class="sxs-lookup"><span data-stu-id="19817-105">Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplyI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="19817-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="19817-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="19817-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="19817-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="19817-108">$n $-bit multiplicando (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="19817-108">$n$-bit multiplicand (LittleEndian)</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="19817-109">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="19817-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="19817-110">multiplicador de $n $-bit (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="19817-110">$n$-bit multiplier (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="19817-111">resultado: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="19817-111">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="19817-112">o resultado de $2n $-bit (LittleEndian) deve estar no estado $ \ket {0} $ inicialmente.</span><span class="sxs-lookup"><span data-stu-id="19817-112">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="19817-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="19817-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="19817-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="19817-114">Remarks</span></span>

<span data-ttu-id="19817-115">Usa uma abordagem de mudança e adição padrão para implementar a multiplicação.</span><span class="sxs-lookup"><span data-stu-id="19817-115">Uses a standard shift-and-add approach to implement the multiplication.</span></span>
<span data-ttu-id="19817-116">A versão controlada foi aprimorada copiando $x _i $ para um ancilla qubit condicionado no controle qubits e, em seguida, controlando a adição no ancilla qubit.</span><span class="sxs-lookup"><span data-stu-id="19817-116">The controlled version was improved by copying out $x_i$ to an ancilla qubit conditioned on the control qubits, and then controlling the addition on the ancilla qubit.</span></span>