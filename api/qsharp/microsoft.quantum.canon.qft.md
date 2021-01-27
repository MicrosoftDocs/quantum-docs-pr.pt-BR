---
uid: Microsoft.Quantum.Canon.QFT
title: Operação QFT
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 30f475c3850c248b5af58db1e4aac3638c4c0471
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852291"
---
# <a name="qft-operation"></a><span data-ttu-id="c190e-102">Operação QFT</span><span class="sxs-lookup"><span data-stu-id="c190e-102">QFT operation</span></span>

<span data-ttu-id="c190e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c190e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c190e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c190e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c190e-105">Executa a transformação de Fourier do Quantum em um registro do Quantum contendo um número inteiro na representação big-endian.</span><span class="sxs-lookup"><span data-stu-id="c190e-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c190e-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c190e-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="c190e-107">QS: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="c190e-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="c190e-108">Quantum registrado para o qual a transformação de Fourier do Quantum é aplicada</span><span class="sxs-lookup"><span data-stu-id="c190e-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="c190e-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c190e-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c190e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c190e-110">Remarks</span></span>

<span data-ttu-id="c190e-111">Presume-se que a entrada e a saída estejam em big endian codificação.</span><span class="sxs-lookup"><span data-stu-id="c190e-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="c190e-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c190e-112">See Also</span></span>

- [<span data-ttu-id="c190e-113">Microsoft. Quantum. Canon. ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="c190e-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)