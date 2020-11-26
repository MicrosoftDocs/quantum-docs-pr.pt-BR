---
uid: Microsoft.Quantum.Math.ModulusL
title: Função de módulo
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 5c9a8ceceac5d2cdac6b82f7f74a85e9443382a2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194926"
---
# <a name="modulusl-function"></a><span data-ttu-id="da410-102">Função de módulo</span><span class="sxs-lookup"><span data-stu-id="da410-102">ModulusL function</span></span>

<span data-ttu-id="da410-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="da410-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="da410-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="da410-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="da410-105">Computa o residue canônico do `value` módulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="da410-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="da410-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="da410-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="da410-107">valor: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="da410-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="da410-108">O valor do qual residue é computado</span><span class="sxs-lookup"><span data-stu-id="da410-108">The value of which residue is computed</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="da410-109">módulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="da410-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="da410-110">O módulo pelo qual residues são tomadas, deve ser positivo</span><span class="sxs-lookup"><span data-stu-id="da410-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--bigint"></a><span data-ttu-id="da410-111">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="da410-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="da410-112">Integer $r $ entre 0 e `modulus - 1` isso `value - r` é divisível por módulo</span><span class="sxs-lookup"><span data-stu-id="da410-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="da410-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="da410-113">Remarks</span></span>

<span data-ttu-id="da410-114">Essa função se comporta de forma diferente de como o operador `%` se comporta em C# e Q # como no resultado é sempre um inteiro positivo entre 0 e `modulus - 1` , mesmo se o valor for negativo.</span><span class="sxs-lookup"><span data-stu-id="da410-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>