---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Operação ApplyQuantumFourierTransform
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: fa8d135c0665f0a576229797d208b321ba0329a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694240"
---
# <a name="applyquantumfouriertransform-operation"></a><span data-ttu-id="ec5f9-102">Operação ApplyQuantumFourierTransform</span><span class="sxs-lookup"><span data-stu-id="ec5f9-102">ApplyQuantumFourierTransform operation</span></span>

<span data-ttu-id="ec5f9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ec5f9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ec5f9-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ec5f9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ec5f9-105">Executa a transformação de Fourier do Quantum em um registro do Quantum contendo um inteiro na representação little-endian.</span><span class="sxs-lookup"><span data-stu-id="ec5f9-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="ec5f9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec5f9-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="ec5f9-107">QS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ec5f9-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ec5f9-108">Quantum registrado para o qual a transformação de Fourier do Quantum é aplicada</span><span class="sxs-lookup"><span data-stu-id="ec5f9-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="ec5f9-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec5f9-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ec5f9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec5f9-110">Remarks</span></span>

<span data-ttu-id="ec5f9-111">Presume-se que a entrada e a saída estejam em little endian codificação.</span><span class="sxs-lookup"><span data-stu-id="ec5f9-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec5f9-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ec5f9-112">See Also</span></span>

- [<span data-ttu-id="ec5f9-113">Microsoft. Quantum. Canon. ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="ec5f9-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)