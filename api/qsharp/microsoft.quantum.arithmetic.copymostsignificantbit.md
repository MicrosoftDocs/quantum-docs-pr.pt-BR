---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Operação CopyMostSignificantBit
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 609e937a03bebf45aa9398225bd1b7e2b717807a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843261"
---
# <a name="copymostsignificantbit-operation"></a><span data-ttu-id="12935-102">Operação CopyMostSignificantBit</span><span class="sxs-lookup"><span data-stu-id="12935-102">CopyMostSignificantBit operation</span></span>

<span data-ttu-id="12935-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="12935-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="12935-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="12935-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="12935-105">Copia o bit mais significativo de um registro qubit `from` que representa um inteiro não assinado no qubit `target` .</span><span class="sxs-lookup"><span data-stu-id="12935-105">Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.</span></span>

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="12935-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="12935-106">Input</span></span>

### <a name="from--littleendian"></a><span data-ttu-id="12935-107">de: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="12935-107">from : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="12935-108">O número inteiro sem sinal do qual o bit mais alto é copiado.</span><span class="sxs-lookup"><span data-stu-id="12935-108">The unsigned integer from which the highest bit is copied from.</span></span>
<span data-ttu-id="12935-109">o inteiro é codificado no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="12935-109">the integer is encoded in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="12935-110">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="12935-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="12935-111">O qubit no qual o bit mais alto está sendo copiado.</span><span class="sxs-lookup"><span data-stu-id="12935-111">The qubit in which the highest bit is being copied.</span></span> <span data-ttu-id="12935-112">A codificação de bits está em base computacional.</span><span class="sxs-lookup"><span data-stu-id="12935-112">The bit encoding is in computational basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="12935-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="12935-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="12935-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="12935-114">See Also</span></span>

- [<span data-ttu-id="12935-115">Microsoft. Quantum. aritmético. LittleEndian</span><span class="sxs-lookup"><span data-stu-id="12935-115">Microsoft.Quantum.Arithmetic.LittleEndian</span></span>](xref:Microsoft.Quantum.Arithmetic.LittleEndian)