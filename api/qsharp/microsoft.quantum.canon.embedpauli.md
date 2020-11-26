---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: Função EmbedPauli
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: e9042ca9eac4b8791057037dc5698eb14deadd31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207030"
---
# <a name="embedpauli-function"></a>Função EmbedPauli

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dado um operador Pauli de qubit único e o índice de um qubit, retorna um operador Pauli de vários qubit com o operador Single-qubit fornecido nesse índice e `PauliI` em todos os outros índices.

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a>Entrada

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Um operador de Pauli de qubit único a ser colocado no local especificado.


### <a name="location--int"></a>local: [int](xref:microsoft.quantum.lang-ref.int)

Um índice de tal forma `output[location] == pauli` , em que `output` é a saída dessa função.


### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Comprimento da matriz a ser retornada.



## <a name="output--pauli"></a>Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

