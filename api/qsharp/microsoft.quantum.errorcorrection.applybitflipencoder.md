---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: Operação ApplyBitFlipEncoder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: 4d78cbb5892aabc600321185641bbf217bd4d745
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693486"
---
# <a name="applybitflipencoder-operation"></a><span data-ttu-id="3abf8-102">Operação ApplyBitFlipEncoder</span><span class="sxs-lookup"><span data-stu-id="3abf8-102">ApplyBitFlipEncoder operation</span></span>

<span data-ttu-id="3abf8-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="3abf8-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="3abf8-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3abf8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3abf8-105">Operação privada usada para implementar o codificador de flip bit e o decodificador.</span><span class="sxs-lookup"><span data-stu-id="3abf8-105">Private operation used to implement both the bit flip encoder and decoder.</span></span>

<span data-ttu-id="3abf8-106">Observe que esse codificador pode fazer uso de recuperação coerente in-loco; nesse caso, ele "causará" o erro descrito pelo estado inicial de `auxQubits` .</span><span class="sxs-lookup"><span data-stu-id="3abf8-106">Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`.</span></span>
<span data-ttu-id="3abf8-107">Em particular, se `auxQubits` estiver inicialmente no estado $ \ket {10} $, isso causará um erro $X _1 $ no qubit codificado.</span><span class="sxs-lookup"><span data-stu-id="3abf8-107">In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.</span></span>

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="3abf8-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="3abf8-108">Input</span></span>

### <a name="coherentrecovery--bool"></a><span data-ttu-id="3abf8-109">coherentRecovery: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3abf8-109">coherentRecovery : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="data--qubit"></a><span data-ttu-id="3abf8-110">dados: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3abf8-110">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="scratch--qubit"></a><span data-ttu-id="3abf8-111">Scratch: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3abf8-111">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="3abf8-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3abf8-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="3abf8-113">Referências</span><span class="sxs-lookup"><span data-stu-id="3abf8-113">References</span></span>

- <span data-ttu-id="3abf8-114">doi:10.1103/PhysRevA.85.044302</span><span class="sxs-lookup"><span data-stu-id="3abf8-114">doi:10.1103/PhysRevA.85.044302</span></span>