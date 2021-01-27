---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC
title: Operação ApplyReversedOpLEC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLEC
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 74ecc705a6e3d1d59c4c4ae71d30171c12fa45ae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843512"
---
# <a name="applyreversedoplec-operation"></a><span data-ttu-id="be1bb-102">Operação ApplyReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="be1bb-102">ApplyReversedOpLEC operation</span></span>

<span data-ttu-id="be1bb-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="be1bb-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="be1bb-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="be1bb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="be1bb-105">Aplica uma operação que usa uma entrada little-endian para uma codificação de registro de um inteiro não assinado usando o formato big endian.</span><span class="sxs-lookup"><span data-stu-id="be1bb-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="be1bb-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="be1bb-106">Input</span></span>

### <a name="op--littleendian--unit--is-ctl"></a><span data-ttu-id="be1bb-107">op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é CTL</span><span class="sxs-lookup"><span data-stu-id="be1bb-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="be1bb-108">Operação que age em um registro little-endian.</span><span class="sxs-lookup"><span data-stu-id="be1bb-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="be1bb-109">registrar: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="be1bb-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="be1bb-110">Um registro big endian a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="be1bb-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="be1bb-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="be1bb-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="be1bb-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="be1bb-112">See Also</span></span>

- [<span data-ttu-id="be1bb-113">Microsoft. Quantum. aritmético. ApplyReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="be1bb-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="be1bb-114">Microsoft. Quantum. aritmético. ApplyReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="be1bb-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="be1bb-115">Microsoft. Quantum. aritmético. ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="be1bb-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)