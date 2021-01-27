---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC
title: Operação ApplyReversedOpBEC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEC
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 7d118d1b04c37a80e61dfab2ee2265b3596b5877
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843551"
---
# <a name="applyreversedopbec-operation"></a><span data-ttu-id="0a088-102">Operação ApplyReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="0a088-102">ApplyReversedOpBEC operation</span></span>

<span data-ttu-id="0a088-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0a088-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0a088-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0a088-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0a088-105">Aplica uma operação que usa a entrada big-endian em uma codificação de registro de um inteiro sem sinal usando o formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="0a088-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="0a088-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0a088-106">Input</span></span>

### <a name="op--bigendian--unit--is-ctl"></a><span data-ttu-id="0a088-107">op: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian é CTL</span><span class="sxs-lookup"><span data-stu-id="0a088-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="0a088-108">Operação que atua em um registro big-endian.</span><span class="sxs-lookup"><span data-stu-id="0a088-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="0a088-109">registrar: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0a088-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0a088-110">Um registro little-endian a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="0a088-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0a088-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0a088-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="0a088-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0a088-112">See Also</span></span>

- [<span data-ttu-id="0a088-113">Microsoft. Quantum. aritmético. ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="0a088-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="0a088-114">Microsoft. Quantum. aritmético. ApplyReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="0a088-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="0a088-115">Microsoft. Quantum. aritmético. ApplyReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="0a088-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)