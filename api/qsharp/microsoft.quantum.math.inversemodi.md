---
uid: Microsoft.Quantum.Math.InverseModI
title: Função InverseModI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 6efc9da5f5ebb64065a90e749daa629dc2dce9cf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696828"
---
# <a name="inversemodi-function"></a><span data-ttu-id="e55f1-102">Função InverseModI</span><span class="sxs-lookup"><span data-stu-id="e55f1-102">InverseModI function</span></span>

<span data-ttu-id="e55f1-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="e55f1-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="e55f1-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e55f1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e55f1-105">Retorna $b $, que $a \cdot b = 1 (\operatorname{mod} \texttt{Modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="e55f1-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="e55f1-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e55f1-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="e55f1-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e55f1-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e55f1-108">O número que está sendo invertido</span><span class="sxs-lookup"><span data-stu-id="e55f1-108">The number being inverted</span></span>


### <a name="modulus--int"></a><span data-ttu-id="e55f1-109">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e55f1-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e55f1-110">O módulo de acordo com o qual os números são invertidos</span><span class="sxs-lookup"><span data-stu-id="e55f1-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--int"></a><span data-ttu-id="e55f1-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e55f1-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e55f1-112">Inteiro $b $, que $a \cdot b = 1 (\operatorname{mod} \texttt{Modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="e55f1-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>