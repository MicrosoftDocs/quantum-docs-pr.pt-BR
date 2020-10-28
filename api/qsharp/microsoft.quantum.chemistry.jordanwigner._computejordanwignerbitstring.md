---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: Função _ComputeJordanWignerBitString
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 31b957a435c3f578bc03d432609cde14c2ef5ced
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693798"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="426d7-102">Função _ComputeJordanWignerBitString</span><span class="sxs-lookup"><span data-stu-id="426d7-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="426d7-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="426d7-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="426d7-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="426d7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="426d7-105">Computa o componente Z da Jordânia – cadeia de caracteres Wigner entre índices Fermion em um operador fermionic com um número par de operadores de criação/Annihilation.</span><span class="sxs-lookup"><span data-stu-id="426d7-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="426d7-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="426d7-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="426d7-107">nFermions: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="426d7-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="426d7-108">O número de fermions no sistema.</span><span class="sxs-lookup"><span data-stu-id="426d7-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="426d7-109">idxFermions: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="426d7-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="426d7-110">índices do operador fermionic.</span><span class="sxs-lookup"><span data-stu-id="426d7-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="426d7-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="426d7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="426d7-112">Bitstring `Bool[]` que é `true` onde um `PauliZ` deve ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="426d7-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>