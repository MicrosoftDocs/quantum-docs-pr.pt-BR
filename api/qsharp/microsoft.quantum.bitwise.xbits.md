---
uid: Microsoft.Quantum.Bitwise.XBits
title: Função XBits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: ddaace8df6e4c47c4affe2eeffb8d8ce31f37327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845241"
---
# <a name="xbits-function"></a><span data-ttu-id="b0e3d-102">Função XBits</span><span class="sxs-lookup"><span data-stu-id="b0e3d-102">XBits function</span></span>

<span data-ttu-id="b0e3d-103">Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="b0e3d-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="b0e3d-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b0e3d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b0e3d-105">Retorna um inteiro que representa os X bits de uma matriz de operadores Pauli.</span><span class="sxs-lookup"><span data-stu-id="b0e3d-105">Returns an integer representing the X bits of an array of Pauli operators.</span></span>

```qsharp
function XBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="b0e3d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0e3d-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="b0e3d-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="b0e3d-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="b0e3d-108">Uma matriz de operadores Pauli a ser representada como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="b0e3d-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="b0e3d-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b0e3d-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b0e3d-110">Um inteiro $x $ com representação binária $ (p_ {62} \, p_ {61} \, \dots \, p_0) $, em que $p _i = $0 se `paulis[i]` for `PauliI` ou `PauliZ` e onde $p _i = $1 se `paulis[i]` for `PauliX` ou `PauliY` .</span><span class="sxs-lookup"><span data-stu-id="b0e3d-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliZ` and where $p_i = 1$ if `paulis[i]` is `PauliX` or `PauliY`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e3d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0e3d-111">Remarks</span></span>

<span data-ttu-id="b0e3d-112">A função gerará se o comprimento da `paulis` matriz for maior que 63.</span><span class="sxs-lookup"><span data-stu-id="b0e3d-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0e3d-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b0e3d-113">See Also</span></span>

- [<span data-ttu-id="b0e3d-114">Microsoft. Quantum. bit-a-ZBits</span><span class="sxs-lookup"><span data-stu-id="b0e3d-114">Microsoft.Quantum.Bitwise.ZBits</span></span>](xref:Microsoft.Quantum.Bitwise.ZBits)