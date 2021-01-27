---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBE
title: Operação ApplyReversedOpBE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBE
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: bf2d43d4e870150f8e6d51dc2f5fb37bdf01d6ec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843604"
---
# <a name="applyreversedopbe-operation"></a><span data-ttu-id="eb43d-102">Operação ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="eb43d-102">ApplyReversedOpBE operation</span></span>

<span data-ttu-id="eb43d-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="eb43d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="eb43d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eb43d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eb43d-105">Aplica uma operação que usa a entrada big-endian em uma codificação de registro de um inteiro sem sinal usando o formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="eb43d-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="eb43d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb43d-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="eb43d-107">op: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian</span><span class="sxs-lookup"><span data-stu-id="eb43d-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="eb43d-108">Operação que atua em um registro big-endian.</span><span class="sxs-lookup"><span data-stu-id="eb43d-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="eb43d-109">registrar: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="eb43d-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="eb43d-110">Um registro little-endian a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="eb43d-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eb43d-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb43d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="eb43d-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="eb43d-112">See Also</span></span>

- [<span data-ttu-id="eb43d-113">Microsoft. Quantum. aritmético. ApplyReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="eb43d-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="eb43d-114">Microsoft. Quantum. aritmético. ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="eb43d-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="eb43d-115">Microsoft. Quantum. aritmético. ApplyReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="eb43d-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)