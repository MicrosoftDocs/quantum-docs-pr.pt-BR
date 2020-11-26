---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBE
title: Função ReversedOpBE
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBE
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 3c39a90ed4b5df09b90d8b5020d8b824285b50eb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222313"
---
# <a name="reversedopbe-function"></a><span data-ttu-id="1e838-102">Função ReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="1e838-102">ReversedOpBE function</span></span>

<span data-ttu-id="1e838-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1e838-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1e838-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1e838-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1e838-105">Dada uma operação que usa uma entrada big-endian, retorna uma nova operação que usa uma entrada little-endian.</span><span class="sxs-lookup"><span data-stu-id="1e838-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="1e838-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e838-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="1e838-107">op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian</span><span class="sxs-lookup"><span data-stu-id="1e838-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="1e838-108">A operação cuja entrada deve ser revertida.</span><span class="sxs-lookup"><span data-stu-id="1e838-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit"></a><span data-ttu-id="1e838-109">Saída: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian</span><span class="sxs-lookup"><span data-stu-id="1e838-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="1e838-110">Uma nova operação que aceita sua entrada como um registro little-endian.</span><span class="sxs-lookup"><span data-stu-id="1e838-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e838-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1e838-111">See Also</span></span>

- [<span data-ttu-id="1e838-112">Microsoft. Quantum. aritmético. ApplyReversedOpBE</span><span class="sxs-lookup"><span data-stu-id="1e838-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="1e838-113">Microsoft. Quantum. aritmético. ReversedOpBEA</span><span class="sxs-lookup"><span data-stu-id="1e838-113">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="1e838-114">Microsoft. Quantum. aritmético. ReversedOpBEC</span><span class="sxs-lookup"><span data-stu-id="1e838-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="1e838-115">Microsoft. Quantum. aritmético. ReversedOpBECA</span><span class="sxs-lookup"><span data-stu-id="1e838-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)