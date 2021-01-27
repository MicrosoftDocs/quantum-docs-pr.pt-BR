---
uid: Microsoft.Quantum.Arithmetic.AddI
title: Operação por
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: a17403652cc2b2712defe52112a3ac599330da9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843839"
---
# <a name="addi-operation"></a><span data-ttu-id="af7f5-102">Operação por</span><span class="sxs-lookup"><span data-stu-id="af7f5-102">AddI operation</span></span>

<span data-ttu-id="af7f5-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="af7f5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="af7f5-104">Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="af7f5-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="af7f5-105">Escolhe automaticamente entre adição e sem, dependendo do tamanho do registro de `ys` .</span><span class="sxs-lookup"><span data-stu-id="af7f5-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="af7f5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="af7f5-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="af7f5-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="af7f5-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="af7f5-108">$n o adendo de $ bit.</span><span class="sxs-lookup"><span data-stu-id="af7f5-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="af7f5-109">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="af7f5-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="af7f5-110">Adendo com pelo menos $n $ qubits.</span><span class="sxs-lookup"><span data-stu-id="af7f5-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="af7f5-111">Manterá o resultado.</span><span class="sxs-lookup"><span data-stu-id="af7f5-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="af7f5-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="af7f5-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

