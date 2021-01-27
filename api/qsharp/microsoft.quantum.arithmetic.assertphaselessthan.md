---
uid: Microsoft.Quantum.Arithmetic.AssertPhaseLessThan
title: Operação AssertPhaseLessThan
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertPhaseLessThan
qsharp.summary: Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.
ms.openlocfilehash: 7b7a4fea8973727da4dcab6f739c6db8da835a2f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843440"
---
# <a name="assertphaselessthan-operation"></a><span data-ttu-id="5180c-102">Operação AssertPhaseLessThan</span><span class="sxs-lookup"><span data-stu-id="5180c-102">AssertPhaseLessThan operation</span></span>

<span data-ttu-id="5180c-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5180c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5180c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5180c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5180c-105">Declara que o `number` codificado em PhaseLittleEndian é menor que `value` .</span><span class="sxs-lookup"><span data-stu-id="5180c-105">Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.</span></span>

```qsharp
operation AssertPhaseLessThan (value : Int, number : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5180c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5180c-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="5180c-107">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5180c-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5180c-108">`number` deve ser menor que isso.</span><span class="sxs-lookup"><span data-stu-id="5180c-108">`number` must be less than this.</span></span>


### <a name="number--phaselittleendian"></a><span data-ttu-id="5180c-109">número: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5180c-109">number : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="5180c-110">Inteiro não assinado que é comparado a `value` .</span><span class="sxs-lookup"><span data-stu-id="5180c-110">Unsigned integer which is compared to `value`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5180c-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5180c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5180c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5180c-112">Remarks</span></span>

<span data-ttu-id="5180c-113">A versão controlada dessa operação ignora os controles.</span><span class="sxs-lookup"><span data-stu-id="5180c-113">The controlled version of this operation ignores controls.</span></span>