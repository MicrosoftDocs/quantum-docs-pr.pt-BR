---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Função EqualityWithinToleranceFact
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: ab7e43d951bf741926b15f27f94d176e88609d4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828744"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="aa8de-102">Função EqualityWithinToleranceFact</span><span class="sxs-lookup"><span data-stu-id="aa8de-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="aa8de-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="aa8de-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="aa8de-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aa8de-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aa8de-105">Representa a declaração de que um valor de ponto flutuante clássico tem o valor esperado até uma determinada tolerância absoluta.</span><span class="sxs-lookup"><span data-stu-id="aa8de-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="aa8de-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa8de-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="aa8de-107">real: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="aa8de-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="aa8de-108">O número a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="aa8de-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="aa8de-109">esperado: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="aa8de-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="aa8de-110">O valor esperado.</span><span class="sxs-lookup"><span data-stu-id="aa8de-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="aa8de-111">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="aa8de-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="aa8de-112">Tolerância absoluta na diferença entre real e esperado.</span><span class="sxs-lookup"><span data-stu-id="aa8de-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aa8de-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aa8de-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

