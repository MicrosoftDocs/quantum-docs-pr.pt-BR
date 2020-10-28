---
uid: Microsoft.Quantum.Bitwise.ZBits
title: Função ZBits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: f66b8ef0370e898dd1d095ff2840c91566f32cb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694353"
---
# <a name="zbits-function"></a>Função ZBits

Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)

Agrupa [](https://nuget.org/packages/)


Retorna um inteiro que representa os bits Z de uma matriz de operadores Pauli.

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a>Entrada

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Uma matriz de operadores Pauli a ser representada como um inteiro.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

Um inteiro $x $ com representação binária $ (p_ {62} \, p_ {61} \, \dots \, p_0) $, em que $p _i = $0 se `paulis[i]` for `PauliI` ou `PauliX` e onde $p _i = $1 se `paulis[i]` for `PauliY` ou `PauliZ` .

## <a name="remarks"></a>Comentários

A função gerará se o comprimento da `paulis` matriz for maior que 63.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. bit-a-XBits](xref:Microsoft.Quantum.Bitwise.XBits)