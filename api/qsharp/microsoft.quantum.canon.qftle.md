---
uid: Microsoft.Quantum.Canon.QFTLE
title: Operação QFTLE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFTLE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: 893366833e5bd6b358884c11f4534609efd72d24
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852269"
---
# <a name="qftle-operation"></a><span data-ttu-id="665e5-102">Operação QFTLE</span><span class="sxs-lookup"><span data-stu-id="665e5-102">QFTLE operation</span></span>

<span data-ttu-id="665e5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="665e5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="665e5-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="665e5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="665e5-105">Executa a transformação de Fourier do Quantum em um registro do Quantum contendo um inteiro na representação little-endian.</span><span class="sxs-lookup"><span data-stu-id="665e5-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation QFTLE (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="665e5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="665e5-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="665e5-107">QS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="665e5-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="665e5-108">Quantum registrado para o qual a transformação de Fourier do Quantum é aplicada</span><span class="sxs-lookup"><span data-stu-id="665e5-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="665e5-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="665e5-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="665e5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="665e5-110">Remarks</span></span>

<span data-ttu-id="665e5-111">Presume-se que a entrada e a saída estejam em little endian codificação.</span><span class="sxs-lookup"><span data-stu-id="665e5-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="665e5-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="665e5-112">See Also</span></span>

- [<span data-ttu-id="665e5-113">Microsoft. Quantum. Canon. QFT</span><span class="sxs-lookup"><span data-stu-id="665e5-113">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)