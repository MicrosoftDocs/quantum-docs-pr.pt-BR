---
uid: Microsoft.Quantum.Canon.Angle
title: Função Angle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: 0528f21b2d9c98b6497e28741964e6497d4d0fb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842046"
---
# <a name="angle-function"></a><span data-ttu-id="32c33-102">Função Angle</span><span class="sxs-lookup"><span data-stu-id="32c33-102">Angle function</span></span>

<span data-ttu-id="32c33-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="32c33-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="32c33-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="32c33-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="32c33-105">Retornará 1, se `index` tiver um número ímpar de 1s e-1, se `index` tiver um número par de 1s.</span><span class="sxs-lookup"><span data-stu-id="32c33-105">Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.</span></span>

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a><span data-ttu-id="32c33-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="32c33-106">Description</span></span>

<span data-ttu-id="32c33-107">O valor corresponde ao sinal do coeficiente do Rademacher-Walsh espectro da variável n e da função para uma determinada Atribuição que decide o ângulo da rotação.</span><span class="sxs-lookup"><span data-stu-id="32c33-107">Value corresponds to the sign of the coefficient of the Rademacher-Walsh spectrum of the n-variable AND function for a given assignment that decides the angle of the rotation.</span></span>

## <a name="input"></a><span data-ttu-id="32c33-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="32c33-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="32c33-109">índice: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="32c33-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="32c33-110">Atribuição de entrada como um inteiro (de 0 a 2 ^ n-1)</span><span class="sxs-lookup"><span data-stu-id="32c33-110">Input assignment as integer (from 0 to 2^n - 1)</span></span>



## <a name="output--int"></a><span data-ttu-id="32c33-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="32c33-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

