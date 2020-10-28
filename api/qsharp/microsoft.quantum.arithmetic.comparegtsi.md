---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Operação CompareGTSI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: 735ae21168d8efb3e626a8f1ea36e97f5cdf8760
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694811"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="31689-102">Operação CompareGTSI</span><span class="sxs-lookup"><span data-stu-id="31689-102">CompareGTSI operation</span></span>

<span data-ttu-id="31689-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="31689-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="31689-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="31689-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="31689-105">Wrapper para comparação de inteiros assinados: `result = xs > ys` .</span><span class="sxs-lookup"><span data-stu-id="31689-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="31689-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="31689-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="31689-107">xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="31689-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="31689-108">Primeiro $n número de $-bit</span><span class="sxs-lookup"><span data-stu-id="31689-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="31689-109">haves: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="31689-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="31689-110">Segundo $n número de $-bit</span><span class="sxs-lookup"><span data-stu-id="31689-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="31689-111">resultado: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="31689-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="31689-112">Será invertido se $xs > haves $</span><span class="sxs-lookup"><span data-stu-id="31689-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="31689-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="31689-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

