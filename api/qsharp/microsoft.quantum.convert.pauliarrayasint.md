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
# <a name="pauliarrayasint-function"></a>Função PauliArrayAsInt

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Codifica um operador qubit Pauli representado como uma matriz de operadores de Pauli de qubit único em um inteiro.

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a>Entrada

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Uma matriz de no máximo 31 operadores de Pauli de qubit único.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

Um inteiro que identifica exclusivamente `paulis` , conforme descrito abaixo.

## <a name="remarks"></a>Comentários

Cada operador Pauli pode ser codificado usando dois bits: $ $ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.
\end{align} $ $

Dada uma matriz de operadores Pauli `[P0, ..., Pn]` , essa função retorna um inteiro com expansão binária formada pela concatenação dos mapeamentos de cada operador Pauli na ordem big-endian `bits(Pn) ... bits(P0)` .