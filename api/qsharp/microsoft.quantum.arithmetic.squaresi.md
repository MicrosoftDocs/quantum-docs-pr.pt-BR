---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: Operação de quadrados
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7fe4d27b974a06b019a2b15710fbc51b598027b4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221820"
---
# <a name="squaresi-operation"></a><span data-ttu-id="391fd-102">Operação de quadrados</span><span class="sxs-lookup"><span data-stu-id="391fd-102">SquareSI operation</span></span>

<span data-ttu-id="391fd-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="391fd-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="391fd-104">Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="391fd-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="391fd-105">Inteiro com sinal de quadrado `xs` e armazena o resultado em `result` , que deve ser inicialmente zero.</span><span class="sxs-lookup"><span data-stu-id="391fd-105">Square signed integer `xs` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="391fd-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="391fd-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="391fd-107">xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="391fd-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="391fd-108">inteiro de n bits para quadrado (SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="391fd-108">n-bit integer to square (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="391fd-109">resultado: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="391fd-109">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="391fd-110">2n-bit Result (SignedLittleEndian), deve estar no estado $ \ket {0} $ inicialmente.</span><span class="sxs-lookup"><span data-stu-id="391fd-110">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="391fd-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="391fd-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="391fd-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="391fd-112">Remarks</span></span>

<span data-ttu-id="391fd-113">A implementação depende do IntegerSquare.</span><span class="sxs-lookup"><span data-stu-id="391fd-113">The implementation relies on IntegerSquare.</span></span>