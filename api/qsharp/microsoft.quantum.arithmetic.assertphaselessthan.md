---
uid: Microsoft.Quantum.Arithmetic.AssertPhaseLessThan
title: Operação AssertPhaseLessThan
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertPhaseLessThan
qsharp.summary: Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.
ms.openlocfilehash: d003d83a84356ce52c5601135000813c7f119e4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694827"
---
# <a name="assertphaselessthan-operation"></a><span data-ttu-id="d1bbe-102">Operação AssertPhaseLessThan</span><span class="sxs-lookup"><span data-stu-id="d1bbe-102">AssertPhaseLessThan operation</span></span>

<span data-ttu-id="d1bbe-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d1bbe-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d1bbe-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d1bbe-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d1bbe-105">Declara que o `number` codificado em PhaseLittleEndian é menor que `value` .</span><span class="sxs-lookup"><span data-stu-id="d1bbe-105">Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.</span></span>

```qsharp
operation AssertPhaseLessThan (value : Int, number : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="d1bbe-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1bbe-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="d1bbe-107">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d1bbe-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d1bbe-108">`number` deve ser menor que isso.</span><span class="sxs-lookup"><span data-stu-id="d1bbe-108">`number` must be less than this.</span></span>


### <a name="number--phaselittleendian"></a><span data-ttu-id="d1bbe-109">número: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d1bbe-109">number : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="d1bbe-110">Inteiro não assinado que é comparado a `value` .</span><span class="sxs-lookup"><span data-stu-id="d1bbe-110">Unsigned integer which is compared to `value`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d1bbe-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d1bbe-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d1bbe-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1bbe-112">Remarks</span></span>

<span data-ttu-id="d1bbe-113">A versão controlada dessa operação ignora os controles.</span><span class="sxs-lookup"><span data-stu-id="d1bbe-113">The controlled version of this operation ignores controls.</span></span>