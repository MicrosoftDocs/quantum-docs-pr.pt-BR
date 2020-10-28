---
uid: Microsoft.Quantum.Canon.QFT
title: Operação QFT
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: e5b40be6c86647205fe1c764b6b043272296a354
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693934"
---
# <a name="qft-operation"></a><span data-ttu-id="c14f9-102">Operação QFT</span><span class="sxs-lookup"><span data-stu-id="c14f9-102">QFT operation</span></span>

<span data-ttu-id="c14f9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c14f9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c14f9-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c14f9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c14f9-105">Executa a transformação de Fourier do Quantum em um registro do Quantum contendo um número inteiro na representação big-endian.</span><span class="sxs-lookup"><span data-stu-id="c14f9-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="c14f9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c14f9-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="c14f9-107">QS: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="c14f9-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="c14f9-108">Quantum registrado para o qual a transformação de Fourier do Quantum é aplicada</span><span class="sxs-lookup"><span data-stu-id="c14f9-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="c14f9-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c14f9-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c14f9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c14f9-110">Remarks</span></span>

<span data-ttu-id="c14f9-111">Presume-se que a entrada e a saída estejam em big endian codificação.</span><span class="sxs-lookup"><span data-stu-id="c14f9-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="c14f9-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c14f9-112">See Also</span></span>

- [<span data-ttu-id="c14f9-113">Microsoft. Quantum. Canon. ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="c14f9-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)