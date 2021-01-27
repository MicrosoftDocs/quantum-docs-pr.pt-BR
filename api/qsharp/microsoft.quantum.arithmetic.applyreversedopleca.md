---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA
title: Operação ApplyReversedOpLECA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLECA
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: d0d444afcc1fa760f3035101e82cf8043c6541c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843491"
---
# <a name="applyreversedopleca-operation"></a><span data-ttu-id="414c2-102">Operação ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="414c2-102">ApplyReversedOpLECA operation</span></span>

<span data-ttu-id="414c2-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="414c2-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="414c2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="414c2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="414c2-105">Aplica uma operação que usa uma entrada little-endian para uma codificação de registro de um inteiro não assinado usando o formato big endian.</span><span class="sxs-lookup"><span data-stu-id="414c2-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl + Adj), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="414c2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="414c2-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="414c2-107">op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="414c2-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="414c2-108">Operação que age em um registro little-endian.</span><span class="sxs-lookup"><span data-stu-id="414c2-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="414c2-109">registrar: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="414c2-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="414c2-110">Um registro big endian a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="414c2-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="414c2-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="414c2-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="414c2-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="414c2-112">See Also</span></span>

- [<span data-ttu-id="414c2-113">Microsoft. Quantum. aritmético. ApplyReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="414c2-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="414c2-114">Microsoft. Quantum. aritmético. ApplyReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="414c2-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="414c2-115">Microsoft. Quantum. aritmético. ApplyReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="414c2-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)