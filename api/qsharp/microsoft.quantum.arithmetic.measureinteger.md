---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Operação MeasureInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 7cd2d93332eb168c7c2be92a3b910033ca8c10ae
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694759"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="35e6c-102">Operação MeasureInteger</span><span class="sxs-lookup"><span data-stu-id="35e6c-102">MeasureInteger operation</span></span>

<span data-ttu-id="35e6c-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="35e6c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="35e6c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="35e6c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="35e6c-105">Mede o conteúdo de um Quantum registrado e o converte em um inteiro.</span><span class="sxs-lookup"><span data-stu-id="35e6c-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="35e6c-106">A medida é executada em relação à base computacional padrão, ou seja, a eigenbasis de `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="35e6c-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="35e6c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="35e6c-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="35e6c-108">destino: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="35e6c-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="35e6c-109">Um registro da Quantum na codificação little-endian.</span><span class="sxs-lookup"><span data-stu-id="35e6c-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="35e6c-110">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="35e6c-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="35e6c-111">Um inteiro sem sinal que contém o valor medido de `target` .</span><span class="sxs-lookup"><span data-stu-id="35e6c-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="35e6c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="35e6c-112">Remarks</span></span>

<span data-ttu-id="35e6c-113">Esta operação redefine seu registro de entrada para o estado $ \ket{00\cdots 0} $, adequado para a liberação de volta para um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="35e6c-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="35e6c-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="35e6c-114">See Also</span></span>

- [<span data-ttu-id="35e6c-115">Microsoft. Quantum. Canon. MeasureIntegerBE</span><span class="sxs-lookup"><span data-stu-id="35e6c-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)