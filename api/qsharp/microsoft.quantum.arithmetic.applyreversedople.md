---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLE
title: Operação ApplyReversedOpLE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLE
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 5f26a25afe5e3d52bae7f7c1b9c8146e5f8a747c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843537"
---
# <a name="applyreversedople-operation"></a><span data-ttu-id="f577f-102">Operação ApplyReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="f577f-102">ApplyReversedOpLE operation</span></span>

<span data-ttu-id="f577f-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f577f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f577f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f577f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f577f-105">Aplica uma operação que usa uma entrada little-endian para uma codificação de registro de um inteiro não assinado usando o formato big endian.</span><span class="sxs-lookup"><span data-stu-id="f577f-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="f577f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f577f-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="f577f-107">op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian</span><span class="sxs-lookup"><span data-stu-id="f577f-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f577f-108">Operação que age em um registro little-endian.</span><span class="sxs-lookup"><span data-stu-id="f577f-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="f577f-109">registrar: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="f577f-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="f577f-110">Um registro big endian a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="f577f-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f577f-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f577f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f577f-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f577f-112">See Also</span></span>

- [<span data-ttu-id="f577f-113">Microsoft. Quantum. aritmético. ApplyReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="f577f-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="f577f-114">Microsoft. Quantum. aritmético. ApplyReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="f577f-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="f577f-115">Microsoft. Quantum. aritmético. ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="f577f-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)