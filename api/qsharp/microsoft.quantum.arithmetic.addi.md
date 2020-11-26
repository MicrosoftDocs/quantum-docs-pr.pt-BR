---
uid: Microsoft.Quantum.Arithmetic.AddI
title: Operação por
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: 9a90d15defd57cf2836a6fda5b52ddaa816fd55e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191016"
---
# <a name="addi-operation"></a><span data-ttu-id="491c5-102">Operação por</span><span class="sxs-lookup"><span data-stu-id="491c5-102">AddI operation</span></span>

<span data-ttu-id="491c5-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="491c5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="491c5-104">Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="491c5-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="491c5-105">Escolhe automaticamente entre adição e sem, dependendo do tamanho do registro de `ys` .</span><span class="sxs-lookup"><span data-stu-id="491c5-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="491c5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="491c5-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="491c5-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="491c5-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="491c5-108">$n o adendo de $ bit.</span><span class="sxs-lookup"><span data-stu-id="491c5-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="491c5-109">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="491c5-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="491c5-110">Adendo com pelo menos $n $ qubits.</span><span class="sxs-lookup"><span data-stu-id="491c5-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="491c5-111">Manterá o resultado.</span><span class="sxs-lookup"><span data-stu-id="491c5-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="491c5-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="491c5-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

