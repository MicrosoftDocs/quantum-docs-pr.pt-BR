---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: Função _ComputeJordanWignerBitString
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 82b5e433f79c93c640b89e6365e5f468bacd892e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839522"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="bf8da-102">Função _ComputeJordanWignerBitString</span><span class="sxs-lookup"><span data-stu-id="bf8da-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="bf8da-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="bf8da-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="bf8da-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="bf8da-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="bf8da-105">Computa o componente Z da Jordânia – cadeia de caracteres Wigner entre índices Fermion em um operador fermionic com um número par de operadores de criação/Annihilation.</span><span class="sxs-lookup"><span data-stu-id="bf8da-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="bf8da-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf8da-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="bf8da-107">nFermions: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bf8da-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bf8da-108">O número de fermions no sistema.</span><span class="sxs-lookup"><span data-stu-id="bf8da-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="bf8da-109">idxFermions: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="bf8da-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="bf8da-110">índices do operador fermionic.</span><span class="sxs-lookup"><span data-stu-id="bf8da-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="bf8da-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="bf8da-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="bf8da-112">Bitstring `Bool[]` que é `true` onde um `PauliZ` deve ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="bf8da-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>

## <a name="example"></a><span data-ttu-id="bf8da-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bf8da-113">Example</span></span>

<span data-ttu-id="bf8da-114">permitir bitString = _ComputeJordanWignerBitString (6, [0, 1, 2, 6]); bitString é [false, false, false, true, true, true, false].</span><span class="sxs-lookup"><span data-stu-id="bf8da-114">let bitString = _ComputeJordanWignerBitString(6, [0,1,2,6]) ; // bitString is [false, false, false ,true, true, true, false].</span></span>