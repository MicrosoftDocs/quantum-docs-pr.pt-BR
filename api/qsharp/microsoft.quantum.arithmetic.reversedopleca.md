---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLECA
title: Função ReversedOpLECA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLECA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: d4245437f2b71abb8bf1bbe4db43ae7d2ee23799
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845745"
---
# <a name="reversedopleca-function"></a><span data-ttu-id="3c99d-102">Função ReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="3c99d-102">ReversedOpLECA function</span></span>

<span data-ttu-id="3c99d-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3c99d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3c99d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3c99d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3c99d-105">Dada uma operação que usa uma entrada little-endian, retorna uma nova operação que usa uma entrada big endian.</span><span class="sxs-lookup"><span data-stu-id="3c99d-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="3c99d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="3c99d-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="3c99d-107">op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="3c99d-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3c99d-108">A operação cuja entrada deve ser revertida.</span><span class="sxs-lookup"><span data-stu-id="3c99d-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="3c99d-109">Saída: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="3c99d-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3c99d-110">Uma nova operação que aceita sua entrada como um registro big endian.</span><span class="sxs-lookup"><span data-stu-id="3c99d-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c99d-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3c99d-111">See Also</span></span>

- [<span data-ttu-id="3c99d-112">Microsoft. Quantum. aritmético. ApplyReversedOpLECA</span><span class="sxs-lookup"><span data-stu-id="3c99d-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)
- [<span data-ttu-id="3c99d-113">Microsoft. Quantum. aritmético. ReversedOpLE</span><span class="sxs-lookup"><span data-stu-id="3c99d-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="3c99d-114">Microsoft. Quantum. aritmético. ReversedOpLEA</span><span class="sxs-lookup"><span data-stu-id="3c99d-114">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="3c99d-115">Microsoft. Quantum. aritmético. ReversedOpLEC</span><span class="sxs-lookup"><span data-stu-id="3c99d-115">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)