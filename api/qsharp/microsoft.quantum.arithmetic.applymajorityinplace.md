---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Operação ApplyMajorityInPlace
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 3664ffe96cd1db8cf5e8898387fe7f2d45b4ea98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694864"
---
# <a name="applymajorityinplace-operation"></a><span data-ttu-id="c26f3-102">Operação ApplyMajorityInPlace</span><span class="sxs-lookup"><span data-stu-id="c26f3-102">ApplyMajorityInPlace operation</span></span>

<span data-ttu-id="c26f3-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c26f3-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c26f3-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c26f3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c26f3-105">Aplica a operação de maioria qubit no local em um registro de qubits.</span><span class="sxs-lookup"><span data-stu-id="c26f3-105">Applies the three-qubit majority operation in-place on a register of qubits.</span></span>

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit
```


## <a name="description"></a><span data-ttu-id="c26f3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c26f3-106">Description</span></span>

<span data-ttu-id="c26f3-107">Esta operação computa a função principal in-loco em 3 qubits.</span><span class="sxs-lookup"><span data-stu-id="c26f3-107">This operation computes the majority function in-place on 3 qubits.</span></span>

<span data-ttu-id="c26f3-108">Se denotarmos qubit de saída como $z $ e qubits de entrada como $x $ e $y $, a operação executará a seguinte transformação: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="c26f3-108">If we denote output qubit as $z$ and input qubits as $x$ and $y$, the operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="c26f3-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c26f3-109">Input</span></span>

### <a name="output--qubit"></a><span data-ttu-id="c26f3-110">saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c26f3-110">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c26f3-111">Primeiro qubit de entrada.</span><span class="sxs-lookup"><span data-stu-id="c26f3-111">First input qubit.</span></span> <span data-ttu-id="c26f3-112">Observe que a saída é calculada in-loco e armazenada neste qubit.</span><span class="sxs-lookup"><span data-stu-id="c26f3-112">Note that the output is computed in-place and stored in this qubit.</span></span>


### <a name="input--qubit"></a><span data-ttu-id="c26f3-113">entrada: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c26f3-113">input : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c26f3-114">Segundo e terceiro qubits de entrada.</span><span class="sxs-lookup"><span data-stu-id="c26f3-114">Second and third input qubits.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c26f3-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c26f3-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

