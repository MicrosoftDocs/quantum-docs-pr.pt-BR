---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: Operação de quadrados
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: c8c4e3cca001aa6d7ce1b9df106ce77f74524301
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694520"
---
# <a name="squaresi-operation"></a><span data-ttu-id="245ed-102">Operação de quadrados</span><span class="sxs-lookup"><span data-stu-id="245ed-102">SquareSI operation</span></span>

<span data-ttu-id="245ed-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="245ed-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="245ed-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="245ed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="245ed-105">Inteiro com sinal de quadrado `xs` e armazena o resultado em `result` , que deve ser inicialmente zero.</span><span class="sxs-lookup"><span data-stu-id="245ed-105">Square signed integer `xs` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="245ed-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="245ed-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="245ed-107">xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="245ed-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="245ed-108">inteiro de n bits para quadrado (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="245ed-108">n-bit integer to square (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="245ed-109">resultado: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="245ed-109">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="245ed-110">2n-bit Result (SignedLittleEndian), deve estar no estado $ \ket {0} $ inicialmente.</span><span class="sxs-lookup"><span data-stu-id="245ed-110">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="245ed-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="245ed-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="245ed-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="245ed-112">Remarks</span></span>

<span data-ttu-id="245ed-113">A implementação depende do IntegerSquare.</span><span class="sxs-lookup"><span data-stu-id="245ed-113">The implementation relies on IntegerSquare.</span></span>