---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Função IdenticalPointPosFactFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 0b285ce980ca1abbc3eb20838389a6f49835e742
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694784"
---
# <a name="identicalpointposfactfxp-function"></a><span data-ttu-id="fe87d-102">Função IdenticalPointPosFactFxP</span><span class="sxs-lookup"><span data-stu-id="fe87d-102">IdenticalPointPosFactFxP function</span></span>

<span data-ttu-id="fe87d-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="fe87d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="fe87d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fe87d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fe87d-105">Declare que todos os números de ponto fixo na matriz fornecida têm posições de ponto idênticas ao contar do bit menos significativo.</span><span class="sxs-lookup"><span data-stu-id="fe87d-105">Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit.</span></span> <span data-ttu-id="fe87d-106">Ou seja, o número de bits e a posição do ponto de menos deve ser constante para todos os números de ponto fixo na matriz.</span><span class="sxs-lookup"><span data-stu-id="fe87d-106">I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.</span></span>

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a><span data-ttu-id="fe87d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe87d-107">Input</span></span>

### <a name="fixedpoints--fixedpoint"></a><span data-ttu-id="fe87d-108">fixedPoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span><span class="sxs-lookup"><span data-stu-id="fe87d-108">fixedPoints : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span></span>

<span data-ttu-id="fe87d-109">Matriz de números de ponto fixo Quantum que serão verificados quanto à compatibilidade (usando asserções).</span><span class="sxs-lookup"><span data-stu-id="fe87d-109">Array of quantum fixed-point numbers that will be checked for compatibility (using assertions).</span></span>



## <a name="output--unit"></a><span data-ttu-id="fe87d-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fe87d-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

