---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC
title: Operação ApplyReversedOpLEC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLEC
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: ac9a6000140445a457a9abc46d5143dcb089883e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694839"
---
# <a name="applyreversedoplec-operation"></a><span data-ttu-id="73067-102">Operação ApplyReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="73067-102">ApplyReversedOpLEC operation</span></span>

<span data-ttu-id="73067-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="73067-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="73067-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="73067-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="73067-105">Aplica uma operação que usa uma entrada little-endian para uma codificação de registro de um inteiro não assinado usando o formato big endian.</span><span class="sxs-lookup"><span data-stu-id="73067-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="73067-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="73067-106">Input</span></span>

### <a name="op--littleendian--unit-ctl"></a><span data-ttu-id="73067-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian</span><span class="sxs-lookup"><span data-stu-id="73067-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="73067-108">Operação que age em um registro little-endian.</span><span class="sxs-lookup"><span data-stu-id="73067-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="73067-109">registrar: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="73067-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="73067-110">Um registro big endian a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="73067-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="73067-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="73067-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="73067-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="73067-112">See Also</span></span>

- [<span data-ttu-id="73067-113">Microsoft. Quantum. aritmético. ApplyReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="73067-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="73067-114">Microsoft. Quantum. aritmético. ApplyReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="73067-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="73067-115">Microsoft. Quantum. aritmético. ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="73067-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)