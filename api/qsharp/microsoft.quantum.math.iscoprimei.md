---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: Função IsCoprimeI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: 2c110f9abf18ee81bd72a68601d5c41ff756290a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851359"
---
# <a name="iscoprimei-function"></a><span data-ttu-id="1596d-102">Função IsCoprimeI</span><span class="sxs-lookup"><span data-stu-id="1596d-102">IsCoprimeI function</span></span>

<span data-ttu-id="1596d-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="1596d-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="1596d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1596d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1596d-105">Retornará true se $a $ e $b $ forem coprimos e false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="1596d-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="1596d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1596d-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="1596d-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1596d-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1596d-108">o primeiro número de que coprimality está sendo testado</span><span class="sxs-lookup"><span data-stu-id="1596d-108">the first number of which co-primality is being tested</span></span>


### <a name="b--int"></a><span data-ttu-id="1596d-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1596d-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1596d-110">o segundo número do qual coprimality está sendo testado</span><span class="sxs-lookup"><span data-stu-id="1596d-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="1596d-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1596d-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1596d-112">True, se $a $ e $b $ forem coprimos (por exemplo, seu maior divisor comum é 1) e false caso contrário</span><span class="sxs-lookup"><span data-stu-id="1596d-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>