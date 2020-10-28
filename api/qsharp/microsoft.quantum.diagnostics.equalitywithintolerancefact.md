---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Função EqualityWithinToleranceFact
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: de15a32d5b38c5ab8c681d2c052669a48cf676cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693519"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="e11be-102">Função EqualityWithinToleranceFact</span><span class="sxs-lookup"><span data-stu-id="e11be-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="e11be-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="e11be-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="e11be-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e11be-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e11be-105">Representa a declaração de que um valor de ponto flutuante clássico tem o valor esperado até uma determinada tolerância absoluta.</span><span class="sxs-lookup"><span data-stu-id="e11be-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="e11be-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e11be-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="e11be-107">real: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e11be-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e11be-108">O número a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="e11be-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="e11be-109">esperado: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e11be-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e11be-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="e11be-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="e11be-111">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e11be-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e11be-112">Tolerância absoluta na diferença entre real e esperado.</span><span class="sxs-lookup"><span data-stu-id="e11be-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e11be-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e11be-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

