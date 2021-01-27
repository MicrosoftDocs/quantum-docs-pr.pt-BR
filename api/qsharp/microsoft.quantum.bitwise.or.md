---
uid: Microsoft.Quantum.Bitwise.Or
title: Função or
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Or
qsharp.summary: Returns the bitwise OR of two integers. This performs the same computation as the built-in `|||` operator.
ms.openlocfilehash: 811e7cf64424e8302c5745c4c71d76de50ab8c08
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845274"
---
# <a name="or-function"></a><span data-ttu-id="386f4-102">Função or</span><span class="sxs-lookup"><span data-stu-id="386f4-102">Or function</span></span>

<span data-ttu-id="386f4-103">Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="386f4-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="386f4-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="386f4-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="386f4-105">Retorna o bit e o de dois inteiros.</span><span class="sxs-lookup"><span data-stu-id="386f4-105">Returns the bitwise OR of two integers.</span></span>
<span data-ttu-id="386f4-106">Isso executa a mesma computação que o `|||` operador interno.</span><span class="sxs-lookup"><span data-stu-id="386f4-106">This performs the same computation as the built-in `|||` operator.</span></span>

```qsharp
function Or (a : Int, b : Int) : Int
```


## <a name="input"></a><span data-ttu-id="386f4-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="386f4-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="386f4-108">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="386f4-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="b--int"></a><span data-ttu-id="386f4-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="386f4-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="386f4-110">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="386f4-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="example"></a><span data-ttu-id="386f4-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="386f4-111">Example</span></span>

```qsharp
let a = 248;      //                 11111000₂
let b = 63;       //                 00111111₂
let x = Or(a, b); // x : Int = 255 = 11111111₂.
```

## <a name="remarks"></a><span data-ttu-id="386f4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="386f4-112">Remarks</span></span>

<span data-ttu-id="386f4-113">Consulte o [C# | Para obter](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/or-operator) mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="386f4-113">See the [C# | Operator](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/or-operator) for more details.</span></span>