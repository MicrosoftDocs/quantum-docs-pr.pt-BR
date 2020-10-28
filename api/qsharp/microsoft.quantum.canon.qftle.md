---
uid: Microsoft.Quantum.Canon.QFTLE
title: Operação QFTLE
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFTLE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: f28f74d34fb4688739646da3dc12ae6734eb4ad4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693932"
---
# <a name="qftle-operation"></a><span data-ttu-id="c6220-102">Operação QFTLE</span><span class="sxs-lookup"><span data-stu-id="c6220-102">QFTLE operation</span></span>

<span data-ttu-id="c6220-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c6220-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c6220-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c6220-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c6220-105">Executa a transformação de Fourier do Quantum em um registro do Quantum contendo um inteiro na representação little-endian.</span><span class="sxs-lookup"><span data-stu-id="c6220-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation QFTLE (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="c6220-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c6220-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="c6220-107">QS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c6220-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c6220-108">Quantum registrado para o qual a transformação de Fourier do Quantum é aplicada</span><span class="sxs-lookup"><span data-stu-id="c6220-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="c6220-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c6220-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c6220-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6220-110">Remarks</span></span>

<span data-ttu-id="c6220-111">Presume-se que a entrada e a saída estejam em little endian codificação.</span><span class="sxs-lookup"><span data-stu-id="c6220-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6220-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c6220-112">See Also</span></span>

- [<span data-ttu-id="c6220-113">Microsoft. Quantum. Canon. QFT</span><span class="sxs-lookup"><span data-stu-id="c6220-113">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)