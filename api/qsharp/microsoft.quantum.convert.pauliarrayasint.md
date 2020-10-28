---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: Função PauliArrayAsInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: f8ec468dd0f0cfd0d868dfc79ff715b3b4fc2f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693608"
---
# <a name="pauliarrayasint-function"></a>Função PauliArrayAsInt

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Agrupa [](https://nuget.org/packages/)


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