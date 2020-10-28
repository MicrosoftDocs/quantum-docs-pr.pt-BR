---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Operação CompareUsingRippleCarry
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: 842e7ded1e38f4f6e01e79d2758e30afb85dd349
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694810"
---
# <a name="compareusingripplecarry-operation"></a><span data-ttu-id="c5859-102">Operação CompareUsingRippleCarry</span><span class="sxs-lookup"><span data-stu-id="c5859-102">CompareUsingRippleCarry operation</span></span>

<span data-ttu-id="c5859-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c5859-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c5859-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c5859-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c5859-105">Esta operação testa se um inteiro representado por um registro de qubits é maior que outro inteiro, aplicando um XOR do resultado em um qubit de saída.</span><span class="sxs-lookup"><span data-stu-id="c5859-105">This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.</span></span>

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="c5859-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5859-106">Description</span></span>

<span data-ttu-id="c5859-107">Considerando dois inteiros `x` e `y` armazenados em registros de qubit de tamanho igual, essa operação verifica se eles atendem `x > y` .</span><span class="sxs-lookup"><span data-stu-id="c5859-107">Given two integers `x` and `y` stored in equal-size qubit registers, this operation checks if they satisfy `x > y`.</span></span> <span data-ttu-id="c5859-108">Se for true, 1 será XORed em um qubit de saída.</span><span class="sxs-lookup"><span data-stu-id="c5859-108">If true, 1 is XORed into an output qubit.</span></span> <span data-ttu-id="c5859-109">Caso contrário, 0 será XORed em um qubit de saída.</span><span class="sxs-lookup"><span data-stu-id="c5859-109">Otherwise, 0 is XORed into an output qubit.</span></span>
<span data-ttu-id="c5859-110">Em outras palavras, essa operação pode ser representada pelo unitário $ $ \begin{align} U\ket {x} \ ket {y} \ ket {z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.</span><span class="sxs-lookup"><span data-stu-id="c5859-110">In other words, this operation can be represented by the unitary $$ \begin{align} U\ket{x}\ket{y}\ket{z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.</span></span>
<span data-ttu-id="c5859-111">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="c5859-111">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="c5859-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5859-112">Input</span></span>

### <a name="x--littleendian"></a><span data-ttu-id="c5859-113">x: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c5859-113">x : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c5859-114">Primeiro número a ser comparado armazenado no `LittleEndian` formato em um registro de qubit.</span><span class="sxs-lookup"><span data-stu-id="c5859-114">First number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="y--littleendian"></a><span data-ttu-id="c5859-115">y: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c5859-115">y : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c5859-116">Segundo número a ser comparado armazenado no `LittleEndian` formato em um registro de qubit.</span><span class="sxs-lookup"><span data-stu-id="c5859-116">Second number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="output--qubit"></a><span data-ttu-id="c5859-117">saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c5859-117">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c5859-118">Qubit que armazena o resultado da comparação $x>y $.</span><span class="sxs-lookup"><span data-stu-id="c5859-118">Qubit that stores the result of the comparison $x>y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c5859-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c5859-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="c5859-120">Referências</span><span class="sxs-lookup"><span data-stu-id="c5859-120">References</span></span>

- <span data-ttu-id="c5859-121">Um novo circuito do Quantum-transporte de adição de Altova-conjunto Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span><span class="sxs-lookup"><span data-stu-id="c5859-121">A new quantum ripple-carry addition circuit Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span></span>