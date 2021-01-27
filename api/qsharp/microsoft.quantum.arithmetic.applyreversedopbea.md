---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA
title: Operação ApplyReversedOpBEA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 1759764947cdbd84a1db945296d441a13f13767e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843596"
---
# <a name="applyreversedopbea-operation"></a><span data-ttu-id="4db73-102">Operação ApplyReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="4db73-102">ApplyReversedOpBEA operation</span></span>

<span data-ttu-id="4db73-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="4db73-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="4db73-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4db73-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4db73-105">Aplica uma operação que usa a entrada big-endian em uma codificação de registro de um inteiro sem sinal usando o formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="4db73-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="4db73-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4db73-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj"></a><span data-ttu-id="4db73-107">op: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian é adj</span><span class="sxs-lookup"><span data-stu-id="4db73-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="4db73-108">Operação que atua em um registro big-endian.</span><span class="sxs-lookup"><span data-stu-id="4db73-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="4db73-109">registrar: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4db73-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="4db73-110">Um registro little-endian a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="4db73-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4db73-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4db73-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="4db73-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4db73-112">See Also</span></span>

- [<span data-ttu-id="4db73-113">Microsoft. Quantum. aritmético. ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="4db73-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="4db73-114">Microsoft. Quantum. aritmético. ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="4db73-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="4db73-115">Microsoft. Quantum. aritmético. ApplyReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="4db73-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)