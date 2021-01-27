---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Operação MeasureInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 288aee24e0ae6425db35312b560630a6bb9bfc80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843114"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="cdfe7-102">Operação MeasureInteger</span><span class="sxs-lookup"><span data-stu-id="cdfe7-102">MeasureInteger operation</span></span>

<span data-ttu-id="cdfe7-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="cdfe7-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="cdfe7-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cdfe7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cdfe7-105">Mede o conteúdo de um Quantum registrado e o converte em um inteiro.</span><span class="sxs-lookup"><span data-stu-id="cdfe7-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="cdfe7-106">A medida é executada em relação à base computacional padrão, ou seja, a eigenbasis de `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="cdfe7-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="cdfe7-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="cdfe7-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="cdfe7-108">destino: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="cdfe7-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="cdfe7-109">Um registro da Quantum na codificação little-endian.</span><span class="sxs-lookup"><span data-stu-id="cdfe7-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="cdfe7-110">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cdfe7-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cdfe7-111">Um inteiro sem sinal que contém o valor medido de `target` .</span><span class="sxs-lookup"><span data-stu-id="cdfe7-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdfe7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdfe7-112">Remarks</span></span>

<span data-ttu-id="cdfe7-113">Esta operação redefine seu registro de entrada para o estado $ \ket{00\cdots 0} $, adequado para a liberação de volta para um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="cdfe7-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="cdfe7-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cdfe7-114">See Also</span></span>

- [<span data-ttu-id="cdfe7-115">Microsoft. Quantum. Canon. MeasureIntegerBE</span><span class="sxs-lookup"><span data-stu-id="cdfe7-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)