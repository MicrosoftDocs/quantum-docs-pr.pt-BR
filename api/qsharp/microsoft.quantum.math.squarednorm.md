---
uid: Microsoft.Quantum.Math.SquaredNorm
title: Função SquaredNorm
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 4165a761753f336cb7b94ad36b11ac324ad4e5c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697026"
---
# <a name="squarednorm-function"></a><span data-ttu-id="f5d60-102">Função SquaredNorm</span><span class="sxs-lookup"><span data-stu-id="f5d60-102">SquaredNorm function</span></span>

<span data-ttu-id="f5d60-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="f5d60-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="f5d60-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f5d60-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f5d60-105">Retorna o quadrado 2-a norma de um vetor.</span><span class="sxs-lookup"><span data-stu-id="f5d60-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="f5d60-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5d60-106">Description</span></span>

<span data-ttu-id="f5d60-107">Retorna o quadrado 2-a norma de um vetor; ou seja, dada uma entrada $ \vec{x} $, retorna $ \ sum_i x_i ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="f5d60-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="f5d60-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5d60-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="f5d60-109">matriz: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f5d60-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f5d60-110">O vetor cujo quadrado 2-normal deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="f5d60-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="f5d60-111">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f5d60-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f5d60-112">O quadrado 2-a norma `array` .</span><span class="sxs-lookup"><span data-stu-id="f5d60-112">The squared 2-norm of `array`.</span></span>