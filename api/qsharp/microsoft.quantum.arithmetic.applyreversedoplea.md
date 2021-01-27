---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA
title: Operação ApplyReversedOpLEA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLEA
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 572841410f16085256fdee9302038cd347476dd9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843523"
---
# <a name="applyreversedoplea-operation"></a><span data-ttu-id="8d321-102">Operação ApplyReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="8d321-102">ApplyReversedOpLEA operation</span></span>

<span data-ttu-id="8d321-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8d321-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8d321-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8d321-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8d321-105">Aplica uma operação que usa uma entrada little-endian para uma codificação de registro de um inteiro não assinado usando o formato big endian.</span><span class="sxs-lookup"><span data-stu-id="8d321-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="8d321-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d321-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj"></a><span data-ttu-id="8d321-107">op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj</span><span class="sxs-lookup"><span data-stu-id="8d321-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="8d321-108">Operação que age em um registro little-endian.</span><span class="sxs-lookup"><span data-stu-id="8d321-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="8d321-109">registrar: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="8d321-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="8d321-110">Um registro big endian a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="8d321-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8d321-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8d321-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="8d321-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8d321-112">See Also</span></span>

- [<span data-ttu-id="8d321-113">Microsoft. Quantum. aritmético. ApplyReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="8d321-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="8d321-114">Microsoft. Quantum. aritmético. ApplyReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="8d321-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="8d321-115">Microsoft. Quantum. aritmético. ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="8d321-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)