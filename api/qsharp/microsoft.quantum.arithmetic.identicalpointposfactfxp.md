---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Função IdenticalPointPosFactFxP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 7212f918e1d0ee86b12b85caa6e0c27bc2cebe58
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846612"
---
# <a name="identicalpointposfactfxp-function"></a><span data-ttu-id="a0e54-102">Função IdenticalPointPosFactFxP</span><span class="sxs-lookup"><span data-stu-id="a0e54-102">IdenticalPointPosFactFxP function</span></span>

<span data-ttu-id="a0e54-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a0e54-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a0e54-104">Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="a0e54-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="a0e54-105">Declare que todos os números de ponto fixo na matriz fornecida têm posições de ponto idênticas ao contar do bit menos significativo.</span><span class="sxs-lookup"><span data-stu-id="a0e54-105">Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit.</span></span> <span data-ttu-id="a0e54-106">Ou seja, o número de bits e a posição do ponto de menos deve ser constante para todos os números de ponto fixo na matriz.</span><span class="sxs-lookup"><span data-stu-id="a0e54-106">I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.</span></span>

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a><span data-ttu-id="a0e54-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0e54-107">Input</span></span>

### <a name="fixedpoints--fixedpoint"></a><span data-ttu-id="a0e54-108">fixedPoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span><span class="sxs-lookup"><span data-stu-id="a0e54-108">fixedPoints : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span></span>

<span data-ttu-id="a0e54-109">Matriz de números de ponto fixo Quantum que serão verificados quanto à compatibilidade (usando asserções).</span><span class="sxs-lookup"><span data-stu-id="a0e54-109">Array of quantum fixed-point numbers that will be checked for compatibility (using assertions).</span></span>



## <a name="output--unit"></a><span data-ttu-id="a0e54-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a0e54-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

