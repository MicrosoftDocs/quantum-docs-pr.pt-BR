---
uid: Microsoft.Quantum.Math.ModulusI
title: Função de móduloi
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6bbb3877b93e1fc6b38f85a716ba617311c7cfba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227770"
---
# <a name="modulusi-function"></a><span data-ttu-id="974b3-102">Função de móduloi</span><span class="sxs-lookup"><span data-stu-id="974b3-102">ModulusI function</span></span>

<span data-ttu-id="974b3-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="974b3-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="974b3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="974b3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="974b3-105">Computa o residue canônico do `value` módulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="974b3-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="974b3-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="974b3-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="974b3-107">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="974b3-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="974b3-108">O valor do qual residue é computado</span><span class="sxs-lookup"><span data-stu-id="974b3-108">The value of which residue is computed</span></span>


### <a name="modulus--int"></a><span data-ttu-id="974b3-109">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="974b3-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="974b3-110">O módulo pelo qual residues são tomadas, deve ser positivo</span><span class="sxs-lookup"><span data-stu-id="974b3-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--int"></a><span data-ttu-id="974b3-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="974b3-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="974b3-112">Integer $r $ entre 0 e `modulus - 1` isso `value - r` é divisível por módulo</span><span class="sxs-lookup"><span data-stu-id="974b3-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="974b3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="974b3-113">Remarks</span></span>

<span data-ttu-id="974b3-114">Essa função se comporta de forma diferente de como o operador `%` se comporta em C# e Q # como no resultado é sempre um inteiro positivo entre 0 e `modulus - 1` , mesmo se o valor for negativo.</span><span class="sxs-lookup"><span data-stu-id="974b3-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>