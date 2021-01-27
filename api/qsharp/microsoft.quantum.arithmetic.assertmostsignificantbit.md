---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Operação AssertMostSignificantBit
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: b0b52a4ba7492d68896669aeb0b6b550d2f27f64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843417"
---
# <a name="assertmostsignificantbit-operation"></a><span data-ttu-id="5a7e5-102">Operação AssertMostSignificantBit</span><span class="sxs-lookup"><span data-stu-id="5a7e5-102">AssertMostSignificantBit operation</span></span>

<span data-ttu-id="5a7e5-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5a7e5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5a7e5-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5a7e5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5a7e5-105">Declara que o qubit mais significativo de um registro de qubit que representa um inteiro não assinado está em um estado específico.</span><span class="sxs-lookup"><span data-stu-id="5a7e5-105">Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.</span></span>

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5a7e5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5a7e5-106">Input</span></span>

### <a name="value--__invalidresult__"></a><span data-ttu-id="5a7e5-107">valor: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="5a7e5-107">value : __invalid<Result>__</span></span>

<span data-ttu-id="5a7e5-108">O valor do maior bit que está sendo declarado.</span><span class="sxs-lookup"><span data-stu-id="5a7e5-108">The value of the highest bit being asserted.</span></span>


### <a name="number--littleendian"></a><span data-ttu-id="5a7e5-109">número: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5a7e5-109">number : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5a7e5-110">Inteiro sem sinal do qual o bit mais alto está marcado.</span><span class="sxs-lookup"><span data-stu-id="5a7e5-110">Unsigned integer of which the highest bit is checked.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5a7e5-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5a7e5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5a7e5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a7e5-112">Remarks</span></span>

<span data-ttu-id="5a7e5-113">A versão controlada dessa operação ignora os controles.</span><span class="sxs-lookup"><span data-stu-id="5a7e5-113">The controlled version of this operation ignores controls.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a7e5-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5a7e5-114">See Also</span></span>

- [<span data-ttu-id="5a7e5-115">Microsoft. Quantum. intrínseca. Assert</span><span class="sxs-lookup"><span data-stu-id="5a7e5-115">Microsoft.Quantum.Intrinsic.Assert</span></span>](xref:Microsoft.Quantum.Intrinsic.Assert)