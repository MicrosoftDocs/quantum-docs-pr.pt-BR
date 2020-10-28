---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBE
title: Operação ApplyReversedOpBE
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBE
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: a181cb16d6ae7684d49fe200d72bcbf5209018e8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694850"
---
# <a name="applyreversedopbe-operation"></a><span data-ttu-id="39995-102">Operação ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="39995-102">ApplyReversedOpBE operation</span></span>

<span data-ttu-id="39995-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="39995-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="39995-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="39995-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="39995-105">Aplica uma operação que usa a entrada big-endian em uma codificação de registro de um inteiro sem sinal usando o formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="39995-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="39995-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="39995-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="39995-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian</span><span class="sxs-lookup"><span data-stu-id="39995-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="39995-108">Operação que atua em um registro big-endian.</span><span class="sxs-lookup"><span data-stu-id="39995-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="39995-109">registrar: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="39995-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="39995-110">Um registro little-endian a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="39995-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39995-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39995-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="39995-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="39995-112">See Also</span></span>

- [<span data-ttu-id="39995-113">Microsoft. Quantum. aritmético. ApplyReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="39995-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="39995-114">Microsoft. Quantum. aritmético. ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="39995-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="39995-115">Microsoft. Quantum. aritmético. ApplyReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="39995-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)