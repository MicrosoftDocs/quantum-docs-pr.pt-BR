---
uid: Microsoft.Quantum.Math.ModulusL
title: Função de módulo
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: e7e692059051fde295634c37892ec54e2cf1b095
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697037"
---
# <a name="modulusl-function"></a><span data-ttu-id="cbdb9-102">Função de módulo</span><span class="sxs-lookup"><span data-stu-id="cbdb9-102">ModulusL function</span></span>

<span data-ttu-id="cbdb9-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="cbdb9-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="cbdb9-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cbdb9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cbdb9-105">Computa o residue canônico do `value` módulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="cbdb9-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="cbdb9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbdb9-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="cbdb9-107">valor: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="cbdb9-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="cbdb9-108">O valor do qual residue é computado</span><span class="sxs-lookup"><span data-stu-id="cbdb9-108">The value of which residue is computed</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="cbdb9-109">módulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="cbdb9-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="cbdb9-110">O módulo pelo qual residues são tomadas, deve ser positivo</span><span class="sxs-lookup"><span data-stu-id="cbdb9-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--bigint"></a><span data-ttu-id="cbdb9-111">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="cbdb9-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="cbdb9-112">Integer $r $ entre 0 e `modulus - 1` isso `value - r` é divisível por módulo</span><span class="sxs-lookup"><span data-stu-id="cbdb9-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="cbdb9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbdb9-113">Remarks</span></span>

<span data-ttu-id="cbdb9-114">Essa função se comporta de forma diferente de como o operador `%` se comporta em C# e Q # como no resultado é sempre um inteiro positivo entre 0 e `modulus - 1` , mesmo se o valor for negativo.</span><span class="sxs-lookup"><span data-stu-id="cbdb9-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>