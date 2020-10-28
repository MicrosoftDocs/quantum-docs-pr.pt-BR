---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Operação AssertMostSignificantBit
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 408e50ed9f2e6c8ba35db20855608d2bd1f24eea
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694828"
---
# <a name="assertmostsignificantbit-operation"></a><span data-ttu-id="a99df-102">Operação AssertMostSignificantBit</span><span class="sxs-lookup"><span data-stu-id="a99df-102">AssertMostSignificantBit operation</span></span>

<span data-ttu-id="a99df-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a99df-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a99df-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a99df-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a99df-105">Declara que o qubit mais significativo de um registro de qubit que representa um inteiro não assinado está em um estado específico.</span><span class="sxs-lookup"><span data-stu-id="a99df-105">Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.</span></span>

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="a99df-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a99df-106">Input</span></span>

### <a name="value--__invalidresult__"></a><span data-ttu-id="a99df-107">valor: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="a99df-107">value : __invalid<Result>__</span></span>

<span data-ttu-id="a99df-108">O valor do maior bit que está sendo declarado.</span><span class="sxs-lookup"><span data-stu-id="a99df-108">The value of the highest bit being asserted.</span></span>


### <a name="number--littleendian"></a><span data-ttu-id="a99df-109">número: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a99df-109">number : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a99df-110">Inteiro sem sinal do qual o bit mais alto está marcado.</span><span class="sxs-lookup"><span data-stu-id="a99df-110">Unsigned integer of which the highest bit is checked.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a99df-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a99df-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a99df-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a99df-112">Remarks</span></span>

<span data-ttu-id="a99df-113">A versão controlada dessa operação ignora os controles.</span><span class="sxs-lookup"><span data-stu-id="a99df-113">The controlled version of this operation ignores controls.</span></span>

## <a name="see-also"></a><span data-ttu-id="a99df-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a99df-114">See Also</span></span>

- [<span data-ttu-id="a99df-115">Microsoft. Quantum. intrínseca. Assert</span><span class="sxs-lookup"><span data-stu-id="a99df-115">Microsoft.Quantum.Intrinsic.Assert</span></span>](xref:Microsoft.Quantum.Intrinsic.Assert)