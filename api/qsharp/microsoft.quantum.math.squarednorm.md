---
uid: Microsoft.Quantum.Math.SquaredNorm
title: Função SquaredNorm
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: ecbc66a8851f23187e0c0ea53ce121442323733b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227294"
---
# <a name="squarednorm-function"></a><span data-ttu-id="fa2e2-102">Função SquaredNorm</span><span class="sxs-lookup"><span data-stu-id="fa2e2-102">SquaredNorm function</span></span>

<span data-ttu-id="fa2e2-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="fa2e2-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="fa2e2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fa2e2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fa2e2-105">Retorna o quadrado 2-a norma de um vetor.</span><span class="sxs-lookup"><span data-stu-id="fa2e2-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="fa2e2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa2e2-106">Description</span></span>

<span data-ttu-id="fa2e2-107">Retorna o quadrado 2-a norma de um vetor; ou seja, dada uma entrada $ \vec{x} $, retorna $ \ sum_i x_i ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="fa2e2-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="fa2e2-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="fa2e2-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="fa2e2-109">matriz: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="fa2e2-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="fa2e2-110">O vetor cujo quadrado 2-normal deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="fa2e2-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="fa2e2-111">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fa2e2-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fa2e2-112">O quadrado 2-a norma `array` .</span><span class="sxs-lookup"><span data-stu-id="fa2e2-112">The squared 2-norm of `array`.</span></span>