---
uid: Microsoft.Quantum.Bitwise.ZBits
title: Função ZBits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: d1ddc2a4cdbdfd3945885de856456b3108592594
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842068"
---
# <a name="zbits-function"></a><span data-ttu-id="d8bdd-102">Função ZBits</span><span class="sxs-lookup"><span data-stu-id="d8bdd-102">ZBits function</span></span>

<span data-ttu-id="d8bdd-103">Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="d8bdd-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="d8bdd-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d8bdd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d8bdd-105">Retorna um inteiro que representa os bits Z de uma matriz de operadores Pauli.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-105">Returns an integer representing the Z bits of an array of Pauli operators.</span></span>

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="d8bdd-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d8bdd-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="d8bdd-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="d8bdd-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="d8bdd-108">Uma matriz de operadores Pauli a ser representada como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="d8bdd-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d8bdd-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d8bdd-110">Um inteiro $x $ com representação binária $ (p_ {62} \, p_ {61} \, \dots \, p_0) $, em que $p _i = $0 se `paulis[i]` for `PauliI` ou `PauliX` e onde $p _i = $1 se `paulis[i]` for `PauliY` ou `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="d8bdd-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliX` and where $p_i = 1$ if `paulis[i]` is `PauliY` or `PauliZ`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8bdd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8bdd-111">Remarks</span></span>

<span data-ttu-id="d8bdd-112">A função gerará se o comprimento da `paulis` matriz for maior que 63.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8bdd-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d8bdd-113">See Also</span></span>

- [<span data-ttu-id="d8bdd-114">Microsoft. Quantum. bit-a-XBits</span><span class="sxs-lookup"><span data-stu-id="d8bdd-114">Microsoft.Quantum.Bitwise.XBits</span></span>](xref:Microsoft.Quantum.Bitwise.XBits)