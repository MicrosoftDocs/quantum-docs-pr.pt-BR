---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA
title: Operação ApplyReversedOpBECA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBECA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 71e99d3390a2e510fd7ed28f3f6d8ed43b3ca7e6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843573"
---
# <a name="applyreversedopbeca-operation"></a><span data-ttu-id="b1dad-102">Operação ApplyReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="b1dad-102">ApplyReversedOpBECA operation</span></span>

<span data-ttu-id="b1dad-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b1dad-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b1dad-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b1dad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b1dad-105">Aplica uma operação que usa a entrada big-endian em uma codificação de registro de um inteiro sem sinal usando o formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="b1dad-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl + Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b1dad-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1dad-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="b1dad-107">op: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="b1dad-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="b1dad-108">Operação que atua em um registro big-endian.</span><span class="sxs-lookup"><span data-stu-id="b1dad-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="b1dad-109">registrar: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b1dad-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b1dad-110">Um registro little-endian a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="b1dad-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b1dad-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b1dad-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="b1dad-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b1dad-112">See Also</span></span>

- [<span data-ttu-id="b1dad-113">Microsoft. Quantum. aritmético. ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="b1dad-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="b1dad-114">Microsoft. Quantum. aritmético. ApplyReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="b1dad-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="b1dad-115">Microsoft. Quantum. aritmético. ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="b1dad-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)