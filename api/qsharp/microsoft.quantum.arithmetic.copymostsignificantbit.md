---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Operação CopyMostSignificantBit
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 02119103fa7b5776f0e1681535115e0773a34c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694800"
---
# <a name="copymostsignificantbit-operation"></a><span data-ttu-id="a0fec-102">Operação CopyMostSignificantBit</span><span class="sxs-lookup"><span data-stu-id="a0fec-102">CopyMostSignificantBit operation</span></span>

<span data-ttu-id="a0fec-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a0fec-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a0fec-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a0fec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a0fec-105">Copia o bit mais significativo de um registro qubit `from` que representa um inteiro não assinado no qubit `target` .</span><span class="sxs-lookup"><span data-stu-id="a0fec-105">Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.</span></span>

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="a0fec-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0fec-106">Input</span></span>

### <a name="from--littleendian"></a><span data-ttu-id="a0fec-107">de: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a0fec-107">from : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a0fec-108">O número inteiro sem sinal do qual o bit mais alto é copiado.</span><span class="sxs-lookup"><span data-stu-id="a0fec-108">The unsigned integer from which the highest bit is copied from.</span></span>
<span data-ttu-id="a0fec-109">o inteiro é codificado no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="a0fec-109">the integer is encoded in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="a0fec-110">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a0fec-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a0fec-111">O qubit no qual o bit mais alto está sendo copiado.</span><span class="sxs-lookup"><span data-stu-id="a0fec-111">The qubit in which the highest bit is being copied.</span></span> <span data-ttu-id="a0fec-112">A codificação de bits está em base computacional.</span><span class="sxs-lookup"><span data-stu-id="a0fec-112">The bit encoding is in computational basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a0fec-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a0fec-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="a0fec-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a0fec-114">See Also</span></span>

- [<span data-ttu-id="a0fec-115">Microsoft. Quantum. aritmético. LittleEndian</span><span class="sxs-lookup"><span data-stu-id="a0fec-115">Microsoft.Quantum.Arithmetic.LittleEndian</span></span>](xref:Microsoft.Quantum.Arithmetic.LittleEndian)