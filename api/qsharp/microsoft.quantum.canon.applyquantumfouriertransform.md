---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Operação ApplyQuantumFourierTransform
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: d99000c21c79d2ca97b1fe92ad331c7ba8599700
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844769"
---
# <a name="applyquantumfouriertransform-operation"></a><span data-ttu-id="cbbc2-102">Operação ApplyQuantumFourierTransform</span><span class="sxs-lookup"><span data-stu-id="cbbc2-102">ApplyQuantumFourierTransform operation</span></span>

<span data-ttu-id="cbbc2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cbbc2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cbbc2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cbbc2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cbbc2-105">Executa a transformação de Fourier do Quantum em um registro do Quantum contendo um inteiro na representação little-endian.</span><span class="sxs-lookup"><span data-stu-id="cbbc2-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cbbc2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbbc2-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="cbbc2-107">QS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="cbbc2-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="cbbc2-108">Quantum registrado para o qual a transformação de Fourier do Quantum é aplicada</span><span class="sxs-lookup"><span data-stu-id="cbbc2-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="cbbc2-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cbbc2-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="cbbc2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbbc2-110">Remarks</span></span>

<span data-ttu-id="cbbc2-111">Presume-se que a entrada e a saída estejam em little endian codificação.</span><span class="sxs-lookup"><span data-stu-id="cbbc2-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbbc2-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cbbc2-112">See Also</span></span>

- [<span data-ttu-id="cbbc2-113">Microsoft. Quantum. Canon. ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="cbbc2-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)