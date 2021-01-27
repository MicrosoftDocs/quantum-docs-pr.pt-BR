---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Operação ApplyQuantumFourierTransformBE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: a1f4a0a5e94465fc8bf3af344e2e19ee0d1d15e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841575"
---
# <a name="applyquantumfouriertransformbe-operation"></a><span data-ttu-id="863d4-102">Operação ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="863d4-102">ApplyQuantumFourierTransformBE operation</span></span>

<span data-ttu-id="863d4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="863d4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="863d4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="863d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="863d4-105">Executa a transformação de Fourier do Quantum em um registro do Quantum contendo um número inteiro na representação big-endian.</span><span class="sxs-lookup"><span data-stu-id="863d4-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="863d4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="863d4-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="863d4-107">QS: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="863d4-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="863d4-108">Quantum registrado para o qual a transformação de Fourier do Quantum é aplicada</span><span class="sxs-lookup"><span data-stu-id="863d4-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="863d4-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="863d4-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="863d4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="863d4-110">Remarks</span></span>

<span data-ttu-id="863d4-111">Presume-se que a entrada e a saída estejam em big endian codificação.</span><span class="sxs-lookup"><span data-stu-id="863d4-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="863d4-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="863d4-112">See Also</span></span>

- [<span data-ttu-id="863d4-113">Microsoft. Quantum. Canon. ApproximateQFT</span><span class="sxs-lookup"><span data-stu-id="863d4-113">Microsoft.Quantum.Canon.ApproximateQFT</span></span>](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [<span data-ttu-id="863d4-114">Microsoft. Quantum. Canon. QFTLE</span><span class="sxs-lookup"><span data-stu-id="863d4-114">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)