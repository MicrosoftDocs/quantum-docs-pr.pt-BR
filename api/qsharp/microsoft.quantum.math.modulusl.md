---
uid: Microsoft.Quantum.Math.ModulusL
title: Função de módulo
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6be2edb052cf55f8e8465c76b5dcadeb61ff11ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842737"
---
# <a name="modulusl-function"></a><span data-ttu-id="aeb87-102">Função de módulo</span><span class="sxs-lookup"><span data-stu-id="aeb87-102">ModulusL function</span></span>

<span data-ttu-id="aeb87-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="aeb87-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="aeb87-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aeb87-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aeb87-105">Computa o residue canônico do `value` módulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="aeb87-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="aeb87-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeb87-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="aeb87-107">valor: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="aeb87-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="aeb87-108">O valor do qual residue é computado</span><span class="sxs-lookup"><span data-stu-id="aeb87-108">The value of which residue is computed</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="aeb87-109">módulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="aeb87-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="aeb87-110">O módulo pelo qual residues são tomadas, deve ser positivo</span><span class="sxs-lookup"><span data-stu-id="aeb87-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--bigint"></a><span data-ttu-id="aeb87-111">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="aeb87-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="aeb87-112">Integer $r $ entre 0 e `modulus - 1` isso `value - r` é divisível por módulo</span><span class="sxs-lookup"><span data-stu-id="aeb87-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="aeb87-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aeb87-113">Remarks</span></span>

<span data-ttu-id="aeb87-114">Essa função se comporta de forma diferente de como o operador `%` se comporta em C# e Q # como no resultado é sempre um inteiro não negativo entre 0 e `modulus - 1` , mesmo se o valor for negativo.</span><span class="sxs-lookup"><span data-stu-id="aeb87-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a non-negative integer between 0 and `modulus - 1`, even if value is negative.</span></span>