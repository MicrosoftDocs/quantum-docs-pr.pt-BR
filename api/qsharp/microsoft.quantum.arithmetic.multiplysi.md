---
uid: Microsoft.Quantum.Arithmetic.MultiplySI
title: Operação MultiplySI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplySI
qsharp.summary: Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 9ca781cbe90a8ec13e6a85a5babaf043bc8f2b5b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694556"
---
# <a name="multiplysi-operation"></a><span data-ttu-id="fe12a-102">Operação MultiplySI</span><span class="sxs-lookup"><span data-stu-id="fe12a-102">MultiplySI operation</span></span>

<span data-ttu-id="fe12a-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="fe12a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="fe12a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fe12a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fe12a-105">Número inteiro assinado multiplicado `xs` por inteiro assinado `ys` e armazena o resultado em `result` , que deve ser inicialmente zero.</span><span class="sxs-lookup"><span data-stu-id="fe12a-105">Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplySI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="fe12a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe12a-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="fe12a-107">xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fe12a-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="fe12a-108">multiplicando de n bits (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fe12a-108">n-bit multiplicand (SignedLittleEndian)</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="fe12a-109">haves: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fe12a-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="fe12a-110">multiplicador de n bits (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fe12a-110">n-bit multiplier (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="fe12a-111">resultado: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fe12a-111">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="fe12a-112">2n-bit Result (SignedLittleEndian), deve estar no estado $ \ket {0} $ inicialmente.</span><span class="sxs-lookup"><span data-stu-id="fe12a-112">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fe12a-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fe12a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
