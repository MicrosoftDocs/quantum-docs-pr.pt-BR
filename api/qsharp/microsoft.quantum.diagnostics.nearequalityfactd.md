---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Função NearEqualityFactD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5b55f515b27667071218a3f604ef703a6a15206d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693505"
---
# <a name="nearequalityfactd-function"></a><span data-ttu-id="397ba-102">Função NearEqualityFactD</span><span class="sxs-lookup"><span data-stu-id="397ba-102">NearEqualityFactD function</span></span>

<span data-ttu-id="397ba-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="397ba-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="397ba-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="397ba-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="397ba-105">Declara que um valor de ponto flutuante clássico tem o valor esperado até uma pequena tolerância de 1e-10.</span><span class="sxs-lookup"><span data-stu-id="397ba-105">Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="397ba-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="397ba-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="397ba-107">real: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="397ba-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="397ba-108">O número a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="397ba-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="397ba-109">esperado: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="397ba-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="397ba-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="397ba-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="397ba-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="397ba-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="397ba-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="397ba-112">Remarks</span></span>

<span data-ttu-id="397ba-113">Isso é equivalente a <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> com a tolerância codificada de $10 ^ {-10} $.</span><span class="sxs-lookup"><span data-stu-id="397ba-113">This is equivalent to <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> with hardcoded tolerance of $10^{-10}$.</span></span>