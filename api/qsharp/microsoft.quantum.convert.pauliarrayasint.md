---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: Função PauliArrayAsInt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: 6077110cc07c8626b22eb404c1de096ed43efcc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224234"
---
# <a name="pauliarrayasint-function"></a><span data-ttu-id="67b0c-102">Função PauliArrayAsInt</span><span class="sxs-lookup"><span data-stu-id="67b0c-102">PauliArrayAsInt function</span></span>

<span data-ttu-id="67b0c-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="67b0c-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="67b0c-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="67b0c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="67b0c-105">Codifica um operador qubit Pauli representado como uma matriz de operadores de Pauli de qubit único em um inteiro.</span><span class="sxs-lookup"><span data-stu-id="67b0c-105">Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.</span></span>

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="67b0c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="67b0c-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="67b0c-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="67b0c-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="67b0c-108">Uma matriz de no máximo 31 operadores de Pauli de qubit único.</span><span class="sxs-lookup"><span data-stu-id="67b0c-108">An array of at most 31 single-qubit Pauli operators.</span></span>



## <a name="output--int"></a><span data-ttu-id="67b0c-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="67b0c-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="67b0c-110">Um inteiro que identifica exclusivamente `paulis` , conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="67b0c-110">An integer uniquely identifying `paulis`, as described below.</span></span>

## <a name="remarks"></a><span data-ttu-id="67b0c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="67b0c-111">Remarks</span></span>

<span data-ttu-id="67b0c-112">Cada operador Pauli pode ser codificado usando dois bits: $ $ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.</span><span class="sxs-lookup"><span data-stu-id="67b0c-112">Each Pauli operator can be encoded using two bits: $$ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.</span></span>
<span data-ttu-id="67b0c-113">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="67b0c-113">\end{align} $$</span></span>

<span data-ttu-id="67b0c-114">Dada uma matriz de operadores Pauli `[P0, ..., Pn]` , essa função retorna um inteiro com expansão binária formada pela concatenação dos mapeamentos de cada operador Pauli na ordem big-endian `bits(Pn) ... bits(P0)` .</span><span class="sxs-lookup"><span data-stu-id="67b0c-114">Given an array of Pauli operators `[P0, ..., Pn]`, this function returns an integer with binary expansion formed by concatenating the mappings of each Pauli operator in big-endian order `bits(Pn) ... bits(P0)`.</span></span>