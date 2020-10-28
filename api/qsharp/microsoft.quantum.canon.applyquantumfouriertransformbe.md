---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Operação ApplyQuantumFourierTransformBE
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: d15310298dc138bdffb612895bbf20ca1371db6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694239"
---
# <a name="applyquantumfouriertransformbe-operation"></a><span data-ttu-id="e6777-102">Operação ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="e6777-102">ApplyQuantumFourierTransformBE operation</span></span>

<span data-ttu-id="e6777-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e6777-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e6777-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e6777-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e6777-105">Executa a transformação de Fourier do Quantum em um registro do Quantum contendo um número inteiro na representação big-endian.</span><span class="sxs-lookup"><span data-stu-id="e6777-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="e6777-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6777-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="e6777-107">QS: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="e6777-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="e6777-108">Quantum registrado para o qual a transformação de Fourier do Quantum é aplicada</span><span class="sxs-lookup"><span data-stu-id="e6777-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="e6777-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e6777-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e6777-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6777-110">Remarks</span></span>

<span data-ttu-id="e6777-111">Presume-se que a entrada e a saída estejam em big endian codificação.</span><span class="sxs-lookup"><span data-stu-id="e6777-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6777-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e6777-112">See Also</span></span>

- [<span data-ttu-id="e6777-113">Microsoft. Quantum. Canon. ApproximateQFT</span><span class="sxs-lookup"><span data-stu-id="e6777-113">Microsoft.Quantum.Canon.ApproximateQFT</span></span>](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [<span data-ttu-id="e6777-114">Microsoft. Quantum. Canon. QFTLE</span><span class="sxs-lookup"><span data-stu-id="e6777-114">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)